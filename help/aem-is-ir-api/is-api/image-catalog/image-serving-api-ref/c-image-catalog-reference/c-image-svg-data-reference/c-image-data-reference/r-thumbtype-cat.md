---
description: Tipo de miniatura. Descreve como uma miniatura para esta imagem deve ser gerada.
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a90b587d-6893-44e4-8dce-7676bc7eebe3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# ThumbType{#thumbtype}

Tipo de miniatura. Descreve como uma miniatura para esta imagem deve ser gerada.

Os seguintes tipos de miniaturas são compatíveis:

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Cortar (1) </p></td> 
  <td class="stentry"> <p>Cortar a imagem na taxa de proporção da miniatura. A menos que a proporção do retângulo da miniatura e da imagem sejam exatamente as mesmas, uma parte da imagem é cortada para garantir que todo o retângulo da miniatura seja preenchido com dados de imagem. O retângulo de recorte está posicionado na imagem usando o atributo <span class="codeph">::ThumbHorizAlign</span> e o atributo <span class="codeph">::ThumbVertAlign</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Ajuste (2) </p></td> 
  <td class="stentry"> <p>Ajustar a imagem inteira no retângulo da miniatura. A imagem está posicionada no retângulo de miniaturas usando o atributo <span class="codeph">::ThumbHorizAlign</span> e o atributo <span class="codeph">::ThumbVertAlign</span>, e qualquer espaço extra é preenchido com o atributo <span class="codeph">::ThumbBkgColor</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Textura (3) </p></td> 
  <td class="stentry"> <p>Recortar a imagem com base na resolução. A imagem é dimensionada pela proporção de <span class="codeph"> catálogo::ThumbRes</span> para <span class="codeph"> catálogo::Resolution</span>. Se a imagem resultante for maior que a miniatura, ela será cortada para caber, se a imagem dimensionada for menor que a miniatura, a área restante será preenchida com o atributo <span class="codeph">::ThumbBkgColor</span>. O atributo <span class="codeph">::ThumbHorizAlign</span> e o atributo <span class="codeph">::ThumbVertAlign</span> são usados para determinar a posição do retângulo de recorte em uma imagem maior ou a posição de uma imagem menor na miniatura. </p></td> 
 </tr> 
</table>

Os clientes solicitam miniaturas de imagem com `req=tmb` solicitações.

## Propriedades {#section-c58a8e67c2134ca3a0edd21b20dd3052}

Valor de Enumeração. Os valores válidos são 1, 2 ou 3, que correspondem aos tipos Corte Demarcado, Ajuste e Textura, respectivamente.

## Padrão {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` é usado se o campo não estiver presente, se o valor for 0 ou se o campo estiver vazio.

## Consulte também {#section-fc1a79d3e6274b4381a17da159649a07}

[attribute::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5), [attribute::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e), [attribute::ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691), [attribute::ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f), [catalog::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69), [catalog::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1), [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Escala de Miniaturas](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
