---
description: O Servidor de imagens suporta arquivos Scalable Vetor Graphics (SVG) como dados de origem. É exigida a conformidade com o SVG 1.1.
solution: Experience Manager
title: suporte para SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# suporte para SVG{#svg-support}

O Servidor de imagens suporta arquivos Scalable Vetor Graphics (SVG) como dados de origem. É exigida a conformidade com o SVG 1.1.

O Servidor de imagens reconhece apenas conteúdos de SVG estáticos; animações, scripts e outros conteúdos interativos não são suportados.

O SVG pode ser especificado sempre que os arquivos de imagem forem permitidos (caminho de URL, `src=` e `mask=`). Depois que o conteúdo do arquivo SVG é rasterizado, ele é manipulado como uma imagem.

Semelhante às imagens, os arquivos SVG podem ser especificados como entradas do catálogo de imagens ou como caminhos de arquivos relativos.

## Variáveis de substituição {#section-83b149f13f244193901df39b204c975b}

As variáveis de substituição ` $ *[!DNL var]*$` podem ser incluídas no arquivo SVG nos elementos `<text>` das cadeias de caracteres de valor e em qualquer atributo de elemento.

As Variáveis importantes na parte de consulta das solicitações incorporadas do Servidor de imagens não são substituídas diretamente. Em vez disso, todas as definições de variáveis disponíveis são anexadas à solicitação, o que permite que o Servidor de imagens substitua variáveis ao analisar a solicitação.

Consulte [Variáveis de Substituição](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) para obter mais informações.

## Referências de imagem {#section-a7680f9e6aca4b1a83560637cc9fac66}

As imagens podem ser inseridas no SVG usando o elemento `<image>`. As imagens referenciadas pelo atributo `xlink::href` do elemento `<image>` devem ser solicitações de servidor de imagens válidas. URLs estrangeiros não são permitidos.

Especifique uma solicitação completa do Servidor de imagens, começando com `http://`, ou uma URL relativa, começando com `/is/image`. Se um caminho HTTP completo for especificado, o nome do domínio será removido do caminho para conversão no formato relativo. O uso de um caminho HTTP completo pode ser uma vantagem, pois permite que o arquivo seja visualizado com um renderizador de SVG de terceiros.

>[!NOTE]
>
>O suporte para renderização de imagens nesta versão do Servidor de imagens é limitado. A referência de imagens no SVG deve ser usada somente em situações em que os mecanismos tradicionais de disposição em camadas e modelos do Servidor de imagens são insuficientes para atingir o resultado desejado. Em nenhuma circunstância o SVG deve ser usado para gerar compostos de várias imagens.

>[!NOTE]
>
>As imagens incorporadas no SVG não são redimensionadas automaticamente no momento. Verifique se todos os hrefs de imagem incluem os comandos do Servidor de imagens necessários para definir o tamanho da imagem desejado (por exemplo, `wid=`). Se o tamanho da imagem não estiver definido explicitamente, `attribute::DefaultPix` será aplicado.

## Gerenciamento de cores {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Pressupõe-se que todos os valores de cores incorporados aos arquivos SVG e passados aos modelos SVG por meio de variáveis de substituição existam no espaço de cores `sRgb`.

Nenhuma conversão de cores é executada quando as imagens são incorporadas no SVG. Para garantir a fidelidade da cor, especifique `icc=sRgb` para todas as solicitações de imagem inseridas.

Após a rasterização, a imagem de SVG participa do gerenciamento de cores como qualquer outra imagem.

## Exemplo {#section-036cdd45abd449849ee00a8f21788c28}

O modelo de SVG a seguir ilustra as referências de imagem e o uso de variáveis.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Esse template de SVG pode ser usado da seguinte maneira:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrições {#section-daa5eccd07204aaf993be41e87822d54}

Os arquivos SVG devem ser independentes e não devem fazer referência a arquivos ou recursos secundários, com exceção das imagens externas referenciadas com as solicitações do Servidor de imagens ou de Renderização de imagens (veja acima).

Somente o conteúdo estático é renderizado. Animação, recursos interativos, como botões e assim por diante. pode estar presente, mas pode não ser renderizado conforme esperado.

As especificações de cores baseadas em perfis ICC não são compatíveis no momento.

`<script>` elementos podem estar presentes, mas são sempre ignorados.

## Consulte também {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [Especificação de SVG 1.1](https://www.w3.org/TR/SVG11/)
