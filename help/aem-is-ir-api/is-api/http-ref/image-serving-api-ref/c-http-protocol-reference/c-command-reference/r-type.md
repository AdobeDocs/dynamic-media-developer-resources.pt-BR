---
description: Filtro de tipo de conteúdo estático. Especifica uma string de filtro para conteúdo estático entregue via /is/content.
solution: Experience Manager
title: type
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---


# type{#type}

Filtro de tipo de conteúdo estático. Especifica uma string de filtro para conteúdo estático entregue via /is/content.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Digite a string do filtro. </p></td> 
 </tr> 
</table>

O servidor comparará o valor com o valor `catalog::Type` do item de conteúdo estático solicitado. O item é retornado ao cliente se os valores corresponderem (diferencia maiúsculas de minúsculas); caso contrário, um erro é retornado.

## Propriedades {#section-529b088434a44a9f86a64ef548d2925b}

Somente suportado para solicitações de conteúdo estático (não imagens) veiculadas por meio de . Ignorado se `catalog::Type` estiver vazio ou não estiver definido.

## Padrão {#section-e9e8f51d0a01452183ccb510efd87d46}

Nenhuma correspondência de tipo é aplicada se `type=` não for especificado ou estiver vazio.

## Consulte também {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Fornecendo Conteúdo Estático (Não Imagem)](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da),  [catálogo::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
