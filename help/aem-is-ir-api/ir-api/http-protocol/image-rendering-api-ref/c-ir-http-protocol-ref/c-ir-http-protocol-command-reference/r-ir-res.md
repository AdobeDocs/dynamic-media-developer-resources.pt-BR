---
description: Resolução de material. Especifica a resolução da textura repetível ou da imagem de decalque.
seo-description: Resolução de material. Especifica a resolução da textura repetível ou da imagem de decalque.
seo-title: res
solution: Experience Manager
title: res
topic: Scene7 Image Serving - Image Rendering API
uuid: ae755a92-ad06-4cf2-b627-0b8b14e385c3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# res{#res}

Resolução de material. Especifica a resolução da textura repetível ou da imagem de decalque.

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Resolução; unidades de resolução de material (tipicamente pixels por polegada) (real). </p> </td> 
 </tr> 
</table>

No caso de um material decal, `size=` prevalece se `size=` e `res=` forem especificados.

## Propriedades {#section-6a458ddc202f46e0b668c9f040a65cef}

Atributo material. Ignorados por materiais de cor sólida. Apenas materiais de revestimento de gabinete e de janela se também for utilizada uma textura.

## Padrão {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`, se o material for baseado em uma entrada de catálogo, caso contrário  `attribute::Resolution`, se  `res= is` não for especificado ou se for definido como um valor menor ou igual a 0.

## Consulte também {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[Resolução](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b) de material,  [tamanho=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988),  [catálogo::Resolução](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7),  [atributo::Resolução](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
