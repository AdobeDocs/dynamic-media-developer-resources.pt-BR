---
title: type
description: Filtro de tipo de conteúdo estático. Especifica uma cadeia de caracteres de filtro para conteúdo estático entregue por meio de /is/content.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# type{#type}

Filtro de tipo de conteúdo estático. Especifica uma cadeia de caracteres de filtro para conteúdo estático entregue por meio de /is/content.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Digite a sequência de caracteres do filtro. </p></td> 
 </tr> 
</table>

O servidor compara `val` com o valor de `catalog::Type` do item de conteúdo estático solicitado. O item é retornado ao cliente se os valores corresponderem (diferencia maiúsculas de minúsculas); caso contrário, um erro é retornado.

## Propriedades {#section-529b088434a44a9f86a64ef548d2925b}

Compatível somente com solicitações de conteúdo estático (não imagens) fornecidas por meio de. Ignorado se `catalog::Type` está vazio ou não está definido.

## Padrão {#section-e9e8f51d0a01452183ccb510efd87d46}

Nenhuma correspondência de tipo é aplicada se `type=` não está especificado ou está vazio.

## Consulte também {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Veiculação De Conteúdo Estático (Não Imagem)](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da), [catálogo:::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
