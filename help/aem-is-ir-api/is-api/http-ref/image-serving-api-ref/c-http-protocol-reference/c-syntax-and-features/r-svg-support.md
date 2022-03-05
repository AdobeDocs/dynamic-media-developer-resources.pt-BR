---
description: O Image Serving suporta arquivos de Vetor Gráfico Escalável (SVG) como dados de origem. A conformidade com o SVG 1.1 é necessária.
solution: Experience Manager
title: Suporte a SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# Suporte a SVG{#svg-support}

O Image Serving suporta arquivos de Vetor Gráfico Escalável (SVG) como dados de origem. A conformidade com o SVG 1.1 é necessária.

O Image Serving só reconhece conteúdo estático de SVG; animações, scripts e outros conteúdos interativos não são compatíveis.

SVG pode ser especificado sempre que os arquivos de imagem forem permitidos (caminho do URL, `src=`e `mask=`). Depois que o conteúdo do arquivo SVG é rasterizado, ele é manipulado como uma imagem.

Semelhante a imagens, os arquivos SVG podem ser especificados como entradas de catálogo de imagens ou como caminhos de arquivo relativos.

## Variáveis de substituição {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` variáveis de substituição podem ser incluídas no arquivo SVG nas cadeias de caracteres de valor `<text>` elementos e qualquer atributo de elemento.

Variáveis importantes na parte de consulta de solicitações incorporadas do Image Serving não são substituídas diretamente. Em vez disso, todas as definições de variável disponíveis são anexadas à solicitação, o que permite que o Serviço de imagem substitua variáveis ao analisar a solicitação.

Consulte [Variáveis de substituição](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) para obter mais informações.

## Referências de imagem {#section-a7680f9e6aca4b1a83560637cc9fac66}

As imagens podem ser inseridas no SVG usando a variável `<image>` elemento. Imagens referenciadas pela `xlink::href` do `<image>` O elemento deve ser uma solicitação válida de fornecimento de imagem. URLs estrangeiros não são permitidos.

Especifique uma solicitação completa de Exibição de imagem, começando com `http://`ou um url relativo, começando com `/is/image`. Se um caminho HTTP completo for especificado, o nome do domínio será removido do caminho para conversão para o formato relativo. O uso de um caminho HTTP completo pode ser vantajoso, pois permite que o arquivo seja visualizado com um renderizador de SVG de terceiros.

>[!NOTE]
>
>O suporte para renderização de imagens nesta versão do Serviço de imagem é limitado. As imagens de referência do SVG devem ser usadas apenas em situações em que os mecanismos tradicionais de camadas e modelos do Image Serving são insuficientes para alcançar o resultado desejado. Em nenhuma circunstância o SVG deve ser usado para gerar compósitos com várias imagens.

>[!NOTE]
>
>As imagens incorporadas no SVG não são redimensionadas automaticamente no momento. Certifique-se de que todos os hrefs de imagem incluam os comandos necessários do Image Serving para definir o tamanho de imagem desejado (por exemplo, `wid=`). Se o tamanho da imagem não estiver definido explicitamente, `attribute::DefaultPix` é aplicada.

## Gerenciamento de cores {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Pressupõe-se que todos os valores de cor incorporados em arquivos SVG e passados para modelos SVG por meio de variáveis de substituição existam no `sRgb` espaço de cores.

Nenhuma conversão de cores é executada quando as imagens são incorporadas ao SVG. Para garantir a fidelidade da cor, especifique `icc=sRgb` para todas as solicitações de imagem incorporadas.

Após a rasterização, a imagem SVG participa do gerenciamento de cores como qualquer outra imagem.

## Exemplo {#section-036cdd45abd449849ee00a8f21788c28}

O modelo de SVG a seguir ilustra as referências de imagem e o uso de variáveis.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Esse template de SVG pode ser usado da seguinte maneira:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrições {#section-daa5eccd07204aaf993be41e87822d54}

Os arquivos SVG devem ser independentes e não devem fazer referência a nenhum arquivo ou recurso secundário, com exceção das imagens externas referenciadas com solicitações de Exibição de imagem ou Renderização de imagem (veja acima).

Somente o conteúdo estático é renderizado. Animação, recursos interativos, como botões, etc. pode estar presente, mas não pode ser renderizado conforme esperado.

No momento, as especificações de cores baseadas em perfil ICC não são compatíveis.

`<script>` podem estar presentes, mas são sempre ignorados.

## Consulte também {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [Especificação do SVG 1.1](https://www.w3.org/TR/SVG11/)
