---
description: Imagem de desfoque. Aplica um filtro de desfoque aos dados da imagem.
seo-description: Imagem de desfoque. Aplica um filtro de desfoque aos dados da imagem.
seo-title: op_blur
solution: Experience Manager
title: op_blur
uuid: 8405bbb5-fe09-412e-9b52-0af2c01f48b9
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---


# op_blur{#op-blur}

Imagem de desfoque. Aplica um filtro de desfoque aos dados da imagem.

`op_blur= *`radius`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>Raio do filtro de desfoque em pixels (real 0.100). </p></td> 
 </tr> 
</table>

*`radius`* está em pixels em relação à imagem composta. Também usado para banalizar efeitos da camada.

## Propriedades {#section-92573fe2c07746a7bab93a81fc3d208d}

comando Camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`.

## Padrão {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, sem efeito de desfoque.

## Exemplo {#section-1ebacde68388492eb108ae0fcd7424db}

Desfoque o plano de fundo de uma imagem. Uma imagem de máscara separada é referenciada por `catalog::MaskPath`. Observe que `layer=0`deve ser especificado explicitamente, caso contrário, `op_blur` seria aplicado a toda a imagem composta.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
