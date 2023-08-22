---
title: estender
description: Estender camada. Adiciona margens a uma camada ou recorta o retângulo da camada.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# estender{#extend}

Estender camada. Adiciona margens a uma camada ou recorta o retângulo da camada.

`extend= *`left`*, *`top`*, *`direita`*, *`bottom`*`

`extendN= *`leftN`*, *`topN`*, *`rightN`*, *`bottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> esquerda,superior,inferior,direita</span></span> </p></td> 
  <td class="stentry"> <p>Número de pixels a serem adicionados (ou removidos, se o valor for negativo) na borda esquerda, superior, direita e inferior da camada (int, int, int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>Quantidade de espaço a ser adicionada (ou removida, se o valor for negativo) à borda esquerda, superior, direita e inferior do retângulo da camada, expresso como valores normalizados relativos ao tamanho do retângulo da camada original (real, real, real, real). </p></td> 
 </tr> 
</table>

`extend=` é aplicado à camada *após* a imagem é cortada ( `crop=`) e todas as transformações de camada, incluindo `rotate=`, foram aplicadas.

A área estendida é preenchida com `bgColor=`ou, se não especificado, permanece transparente.

Valores de argumento para `extendN=` são normalizados em relação ao tamanho da camada, diretamente após as transformações, incluindo `rotate=` foram aplicadas.

## Propriedades {#section-8fc94de871f841f3bf5e1df135972ca9}

Atributo de camada. Aplica-se à camada 0 se `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, para que não haja alteração do retângulo da camada.

## Exemplos {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Cortar uma imagem e adicionar uma borda vermelha de 5 pixels de largura:**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Dimensione uma imagem para uma largura de 200 pixels e adicione o texto do título a uma margem de 30 pixels acima da imagem.**

Observe que a altura da imagem composta varia dependendo da proporção da imagem.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## Consulte também {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [origem=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
