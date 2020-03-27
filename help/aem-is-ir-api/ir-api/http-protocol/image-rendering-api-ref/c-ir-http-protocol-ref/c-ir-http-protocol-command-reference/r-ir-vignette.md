---
description: Arquivo de vinheta. Especifica a vinheta a ser usada para esta solicitação.
seo-description: Arquivo de vinheta. Especifica a vinheta a ser usada para esta solicitação.
seo-title: vinheta
solution: Experience Manager
title: vinheta
topic: Scene7 Image Serving - Image Rendering API
uuid: 8bba4ad4-bd55-4c55-8ebf-585371cf33f1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# vinheta{#vignette}

Arquivo de vinheta. Especifica a vinheta a ser usada para esta solicitação.

`vignette=[ *`arquivo`*/] *``*|[catId/] *`catIdentirecIdfile`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>ID do catálogo de material (correspondente ao <span class="codeph"> atributo::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>ID da vinheta (correspondente à <span class="codeph"> vinheta::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> arquivo</span> </p></td> 
  <td class="stentry"> <p>Nome e caminho do arquivo de vinheta relativos. </p></td> 
 </tr> 
</table>

Pode especificar uma entrada do mapa de vinheta ou um arquivo de vinheta. URLs remotos não são permitidos.

`vignette=` pode ser usada como uma alternativa para especificar a vinheta no caminho do URL da solicitação. Usado principalmente para especificar vinhetas por meio de variáveis em modelos.

Se não *`catId`* for especificado, o catálogo de sessão será usado.

## Propriedades {#section-f58661fc78d7496e8e3d0fb98b945c4b}

Pode ocorrer em qualquer lugar dentro da solicitação. Substitui a vinheta especificada pelo caminho do URL da solicitação.

## Padrão {#section-db0618d48bc84dc8abcc989550349ccc}

Nenhum.

## Consulte também {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[Catálogos](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)de materiais, variáveis [personalizadas](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
