---
description: Filtro de tipo de conteúdo estático. Especifica uma string de filtro para o conteúdo estático fornecido por /is/content.
seo-description: Filtro de tipo de conteúdo estático. Especifica uma string de filtro para o conteúdo estático fornecido por /is/content.
seo-title: type
solution: Experience Manager
title: type
topic: Scene7 Image Serving - Image Rendering API
uuid: 44906190-516c-481c-9714-bb19d77af33c
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# type{#type}

Filtro de tipo de conteúdo estático. Especifica uma string de filtro para o conteúdo estático fornecido por /is/content.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Digite a string do filtro. </p></td> 
 </tr> 
</table>

O servidor comparará o valor com o valor do item `catalog::Type` de conteúdo estático solicitado. O item será retornado ao cliente se os valores corresponderem (diferenciando maiúsculas de minúsculas); caso contrário, um erro será retornado.

## Propriedades {#section-529b088434a44a9f86a64ef548d2925b}

Somente suportado para solicitações de conteúdo estático (não imagens) enviadas por meio de. Ignorado se `catalog::Type` estiver vazio ou não estiver definido.

## Padrão {#section-e9e8f51d0a01452183ccb510efd87d46}

Nenhuma correspondência de tipo é aplicada se não `type=` for especificada ou estiver vazia.

## Consulte também {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Servindo conteúdo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da)estático (não imagem), [catálogo::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
