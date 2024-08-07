---
title: res
description: Resolução do material. Especifica a resolução da textura ou imagem de decalque repetível.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f207355d-5819-47fc-bda5-27a411449569
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# res{#res}

Resolução do material. Especifica a resolução da textura ou imagem de decalque repetível.

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Resolução; unidades de resolução do material (normalmente pixels por polegada) (real). </p> </td> 
 </tr> 
</table>

Se houver um material de decalque, `size=` prevalecerá se `size=` e `res=` forem especificados.

## Propriedades {#section-6a458ddc202f46e0b668c9f040a65cef}

Atributo de material. Ignorado por materiais de cores sólidas. Apenas por materiais de revestimentos de armários e janelas se uma textura também for usada.

## Padrão {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`, se o material for baseado em uma entrada de catálogo, caso contrário `attribute::Resolution`, se `res= is` não for especificado ou se estiver definido com um valor menor ou igual a 0.

## Consulte também {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[Resolução de Material](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b), [tamanho=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988), [catálogo::Resolução](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7), [atributo::Resolução](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
