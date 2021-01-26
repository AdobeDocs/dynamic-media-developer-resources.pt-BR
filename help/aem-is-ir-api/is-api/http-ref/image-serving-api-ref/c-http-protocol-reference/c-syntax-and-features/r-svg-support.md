---
description: O Serviço de imagem oferece suporte a arquivos Scalable Vetor Graphics (SVG) como dados de origem. É necessária a conformidade com SVG 1.1.
seo-description: O Serviço de imagem oferece suporte a arquivos Scalable Vetor Graphics (SVG) como dados de origem. É necessária a conformidade com SVG 1.1.
seo-title: Suporte a SVG
solution: Experience Manager
title: Suporte a SVG
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 30d7b37d-fdef-4518-a4b3-4baee56fa634
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---


# Suporte a SVG{#svg-support}

O Serviço de imagem oferece suporte a arquivos Scalable Vetor Graphics (SVG) como dados de origem. É necessária a conformidade com SVG 1.1.

O Serviço de Imagens só reconhece conteúdo SVG estático; animações, scripts e outros conteúdos interativos não são suportados.

O SVG pode ser especificado onde quer que os arquivos de imagem sejam permitidos (caminho do URL, `src=` e `mask=`). Depois que o conteúdo do arquivo SVG é rasterizado, ele é manipulado como uma imagem.

Semelhante às imagens, os arquivos SVG podem ser especificados como entradas de catálogo de imagens ou como caminhos de arquivo relativos.

## Variáveis de substituição {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` variáveis de substituição podem ser incluídas no arquivo SVG nos  `<text>` elementos de strings de valor e em qualquer atributo de elemento.

Variáveis importantes na parte query das solicitações incorporadas do Serviço de imagem não são substituídas diretamente. Em vez disso, todas as definições de variáveis disponíveis são anexadas à solicitação, o que permite que o Serviço de imagem substitua variáveis ao analisar a solicitação.

Consulte [Variáveis de substituição](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) para obter mais informações.

## Referências de imagem {#section-a7680f9e6aca4b1a83560637cc9fac66}

As imagens podem ser inseridas no SVG usando o elemento `<image>`. As imagens referenciadas pelo atributo `xlink::href` do elemento `<image>` devem ser solicitações válidas de serviço de imagem. URLs externos não são permitidos.

Especifique uma solicitação completa de Serviço de imagem, começando com `http://`, ou um url relativo, começando com `/is/image`. Se um caminho HTTP completo for especificado, o nome do domínio será removido do caminho para conversão no formato relativo. O uso de um caminho HTTP completo pode ser vantajoso, pois permite que o arquivo seja visualizado com um renderizador SVG de terceiros.

>[!NOTE]
>
>O suporte para renderizar imagens nesta versão do Serviço de imagens é limitado. As imagens de referência de dentro do SVG devem ser usadas somente em situações em que os mecanismos tradicionais de camada e modelagem do serviço de imagem não sejam suficientes para alcançar o resultado desejado. Em nenhuma circunstância o SVG deve ser usado para gerar compostos de várias imagens.

>[!NOTE]
>
>As imagens incorporadas no SVG não são redimensionadas automaticamente no momento. Certifique-se de que todas as referências de imagem incluam os comandos necessários para Servir de imagem para definir o tamanho de imagem desejado (por exemplo, `wid=`). Se o tamanho da imagem não estiver definido explicitamente, `attribute::DefaultPix` será aplicado.

## Gerenciamento de cores {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Pressupõe-se que todos os valores de cor incorporados em arquivos SVG e passados para modelos SVG por meio de variáveis de substituição existam no espaço de cores `sRgb`.

Nenhuma conversão de cores é realizada quando as imagens são incorporadas ao SVG. Para garantir a fidelidade de cores, especifique `icc=sRgb` para todas as solicitações de imagem incorporadas.

Após a rasterização, a imagem SVG participa do gerenciamento de cores como qualquer outra imagem.

## Exemplo {#section-036cdd45abd449849ee00a8f21788c28}

O seguinte modelo SVG ilustra as referências de imagem e o uso de variáveis.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Esse modelo SVG pode ser usado da seguinte maneira:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrições {#section-daa5eccd07204aaf993be41e87822d54}

Os arquivos SVG devem ser independentes e não devem fazer referência a nenhum arquivo ou recurso secundário, com exceção das imagens externas referenciadas com solicitações de Servidor de imagens ou Renderização de imagens (consulte acima).

Somente o conteúdo estático é renderizado. Animação, recursos interativos, como botões etc. podem estar presentes, mas não podem ser renderizados como esperado.

No momento, não há suporte para especificações de cores baseadas em perfis ICC.

`<script>` podem estar presentes, mas são sempre ignorados.

## Consulte também {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), Especificação  [SVG 1.1](http://www.w3.org/TR/SVG11/)
