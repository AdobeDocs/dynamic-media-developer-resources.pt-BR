---
description: Arquivo Vignette. Especifica a vinheta a ser usada para esta solicitação.
solution: Experience Manager
title: vinheta
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 8419d68d-7579-4e62-abbd-7dc0a736ae23
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# vinheta{#vignette}

Arquivo Vignette. Especifica a vinheta a ser usada para esta solicitação.

`vignette=[ *``*/] *``*|[catId/] *`catIndexIdfile`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>ID do catálogo de materiais (correspondente ao atributo <span class="codeph">::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>ID da vinheta (correspondente a <span class="codeph"> vinheta::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> arquivo</span> </p></td> 
  <td class="stentry"> <p>Caminho e nome do arquivo da vinheta relativa. </p></td> 
 </tr> 
</table>

Pode especificar uma entrada do mapa de vinheta ou um arquivo de vinheta. URLs remotos não são permitidos.

`vignette=` pode ser usada como uma alternativa para especificar a vinheta no caminho do URL da solicitação. Usada principalmente para especificar vinhetas por meio de variáveis em modelos.

Se *`catId`* não for especificado, o catálogo de sessão será usado.

## Propriedades {#section-f58661fc78d7496e8e3d0fb98b945c4b}

Pode ocorrer em qualquer lugar dentro da solicitação. Substitui a vinheta especificada pelo caminho do URL da solicitação.

## Padrão {#section-db0618d48bc84dc8abcc989550349ccc}

Nenhum.

## Consulte também {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[Catálogos](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2) de materiais, variáveis  [personalizadas](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
