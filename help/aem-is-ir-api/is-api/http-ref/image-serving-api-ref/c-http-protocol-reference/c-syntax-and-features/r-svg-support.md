---
description: O Image Serving suporta arquivos SVG (Scalable Vetor Graphics) como dados de origem. É necessária a conformidade com o SVG 1.1.
solution: Experience Manager
title: Suporte SVG
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---


# Suporte a SVG{#svg-support}

O Image Serving suporta arquivos SVG (Scalable Vetor Graphics) como dados de origem. É necessária a conformidade com o SVG 1.1.

O Image Serving reconhece apenas o conteúdo SVG estático; animações, scripts e outros conteúdos interativos não são compatíveis.

O SVG pode ser especificado sempre que os arquivos de imagem forem permitidos (caminho de URL, `src=` e `mask=`). Depois que o conteúdo do arquivo SVG é rasterizado, ele é manipulado como uma imagem.

Semelhante a imagens, os arquivos SVG podem ser especificados como entradas de catálogo de imagens ou como caminhos de arquivo relativos.

## Variáveis de substituição {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` as variáveis de substituição podem ser incluídas no arquivo SVG nos  `<text>` elementos das cadeias de valores e em qualquer atributo de elemento.

Variáveis importantes na parte de consulta de solicitações incorporadas do Image Serving não são substituídas diretamente. Em vez disso, todas as definições de variável disponíveis são anexadas à solicitação, o que permite que o Serviço de imagem substitua variáveis ao analisar a solicitação.

Consulte [Variáveis de substituição](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) para obter mais informações.

## Referência de imagem {#section-a7680f9e6aca4b1a83560637cc9fac66}

As imagens podem ser inseridas no SVG usando o elemento `<image>` . As imagens referenciadas pelo atributo `xlink::href` do elemento `<image>` devem ser solicitações válidas de veiculação de imagens. URLs estrangeiros não são permitidos.

Especifique uma solicitação completa de Exibição de imagem, começando com `http://`, ou um url relativo, começando com `/is/image`. Se um caminho HTTP completo for especificado, o nome do domínio será removido do caminho para conversão para o formato relativo. O uso de um caminho HTTP completo pode ser vantajoso, pois permite que o arquivo seja visualizado com um renderizador SVG de terceiros.

>[!NOTE]
>
>O suporte para renderização de imagens nesta versão do Serviço de imagem é limitado. A referência a imagens de dentro do SVG deve ser usada somente em situações em que os mecanismos tradicionais de camadas e modelos de disponibilização de imagens são insuficientes para alcançar o resultado desejado. Em nenhuma circunstância o SVG deve ser usado para gerar compósitos com várias imagens.

>[!NOTE]
>
>As imagens incorporadas no SVG não são redimensionadas automaticamente no momento. Certifique-se de que todos os hrefs de imagem incluam os comandos necessários do Image Serving para definir o tamanho de imagem desejado (por exemplo, `wid=`). Se o tamanho da imagem não for definido explicitamente, `attribute::DefaultPix` será aplicado.

## Gestão de cores {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Pressupõe-se que todos os valores de cor incorporados em arquivos SVG e passados para modelos SVG por meio de variáveis de substituição existam no espaço de cores `sRgb`.

Nenhuma conversão de cores é executada quando as imagens são incorporadas ao SVG. Para garantir a fidelidade da cor, especifique `icc=sRgb` para todas as solicitações de imagem incorporadas.

Após a rasterização, a imagem SVG participa do gerenciamento de cores como qualquer outra imagem.

## Exemplo {#section-036cdd45abd449849ee00a8f21788c28}

O modelo SVG a seguir ilustra as referências de imagem e o uso das variáveis.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Esse modelo SVG pode ser usado da seguinte maneira:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrições {#section-daa5eccd07204aaf993be41e87822d54}

Os arquivos SVG devem ser independentes e não devem fazer referência a nenhum arquivo ou recurso secundário, com exceção das imagens externas referenciadas com solicitações de Exibição de imagem ou Renderização de imagem (veja acima).

Somente o conteúdo estático é renderizado. Animação, recursos interativos, como botões, etc. pode estar presente, mas não pode ser renderizado conforme esperado.

No momento, as especificações de cores baseadas em perfil ICC não são compatíveis.

`<script>` podem estar presentes, mas são sempre ignorados.

## Consulte também {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), Especificação  [SVG 1.1](http://www.w3.org/TR/SVG11/)
