---
title: vinheta
description: Arquivo de vinheta. Especifica a vinheta a ser usada para a solicitação.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8419d68d-7579-4e62-abbd-7dc0a736ae23
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# vinheta{#vignette}

Arquivo de vinheta. Especifica a vinheta a ser usada para a solicitação.

`vignette=[ *`catId`*/] *`recId`*|[catId/] *`file`*`

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
  <td class="stentry"> <p>Caminho e nome do arquivo de vinheta relativos. </p></td> 
 </tr> 
</table>

Pode especificar uma entrada de mapa de vinheta ou um arquivo de vinheta. URLs remotos não são permitidos.

`vignette=` Pode ser usado como uma alternativa para especificar a vinheta no caminho da URL da solicitação. Usado para especificar vinhetas por meio de variáveis em modelos.

Se *`catId`* não for especificado, o catálogo da sessão será usado.

## Propriedades {#section-f58661fc78d7496e8e3d0fb98b945c4b}

Pode ocorrer em qualquer lugar na solicitação. Substitui a vinheta especificada pelo caminho do URL da solicitação.

## Padrão {#section-db0618d48bc84dc8abcc989550349ccc}

Nenhum.

## Consulte também {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[Catálogos de Materiais](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [Variáveis Personalizadas](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
