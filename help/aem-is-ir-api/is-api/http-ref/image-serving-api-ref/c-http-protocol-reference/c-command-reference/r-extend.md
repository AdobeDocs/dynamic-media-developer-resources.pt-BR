---
description: Estende a camada. Adiciona margens a uma camada ou corta o retângulo da camada.
seo-description: Estende a camada. Adiciona margens a uma camada ou corta o retângulo da camada.
seo-title: extensão
solution: Experience Manager
title: extensão
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ca69994-e788-41a9-93ac-f22b6b9920d0
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# estender{#extend}

Estende a camada. Adiciona margens a uma camada ou corta o retângulo da camada.

`extend= *``*, *``*, *``*, *`left-toprightbottom`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> esquerda,superior,inferior,direita</span></span> </p></td> 
  <td class="stentry"> <p>Número de pixels a adicionar (ou remover de, se o valor for negativo) à borda esquerda, superior, direita e inferior da camada reta (int, int, int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>Quantidade de espaço para adicionar (ou remover de, se o valor for negativo) à borda esquerda, superior, direita e inferior do retângulo da camada, expressa como quantidades normalizadas em relação ao tamanho do retângulo da camada original (real, real, real, real). </p></td> 
 </tr> 
</table>

`extend=` é aplicada à camada  ** depois que a imagem é cortada (  `crop=`) e todas as transformações de camada, incluindo  `rotate=`, foram aplicadas.

A área estendida é preenchida com `bgColor=` ou, se não for especificada, permanece transparente.

Os valores de argumento para `extendN=` são normalizados em relação ao tamanho do retângulo de camada após as transformações de camada, incluindo `rotate=` terem sido aplicados.

## Propriedades {#section-8fc94de871f841f3bf5e1df135972ca9}

Atributo de camada. Aplica-se à camada 0 se `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, sem alteração do retângulo da camada.

## Exemplos {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Recorte uma imagem e adicione uma borda vermelha de 5 pixels de largura:**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Dimensione uma imagem para ter 200 pixels de largura e adicione o texto do título a uma margem de 30 pixels acima da imagem.**

Observe que a altura da imagem composta varia dependendo da proporção da imagem.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## Consulte também {#section-2d9572be32ca4602b60920b3810f3638}

[Recortar=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [cor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [tamanho=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b),  [origem=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
