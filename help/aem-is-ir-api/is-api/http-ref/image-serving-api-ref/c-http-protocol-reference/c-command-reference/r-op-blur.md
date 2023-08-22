---
title: op_blur
description: Imagem de desfoque. Aplica um filtro de desfoque aos dados da imagem.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# op_blur{#op-blur}

Imagem de desfoque. Aplica um filtro de desfoque aos dados da imagem.

`op_blur= *`raio`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> raio</span> </p> </td> 
  <td class="stentry"> <p>Raio do filtro de desfoque em pixels (real 0 a 100). </p></td> 
 </tr> 
</table>

*`radius`* é expresso em pixels em relação à imagem composta. Também usado para difundir efeitos de camada.

## Propriedades {#section-92573fe2c07746a7bab93a81fc3d208d}

Camada. Se aplica à camada atual ou à imagem composta `layer=comp`.

## Padrão {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, para nenhum efeito de desfoque.

## Exemplo {#section-1ebacde68388492eb108ae0fcd7424db}

Desfoca o plano de fundo de uma imagem. Uma imagem de máscara separada é referenciada pelo `catalog::MaskPath`. Observe que `layer=0`deve ser especificado explicitamente, caso contrário `op_blur` será aplicado a toda a imagem composta.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
