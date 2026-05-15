---
title: op_blur
description: Imagem de desfoque. Aplica um filtro de desfoque aos dados da imagem.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
TQID: 'https://experienceleague.adobe.com/e7GXc5NYZC2Flk0Uf71iw-hi-gPdQk-XldMpPH-DwqM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 0%

---

# op_blur{#op-blur}

Imagem de desfoque. Aplica um filtro de desfoque aos dados da imagem.

`op_blur= *`raio`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>Raio do filtro de desfoque em pixels (real 0 a 100). </p></td> 
 </tr> 
</table>

*`radius`* está em pixels relativos à imagem composta. Também usado para difundir efeitos de camada.

## Propriedades {#section-92573fe2c07746a7bab93a81fc3d208d}

Camada. Aplica-se à camada atual ou à imagem composta, se `layer=comp`.

## Padrão {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, para nenhum efeito de desfoque.

## Exemplo {#section-1ebacde68388492eb108ae0fcd7424db}

Desfoca o plano de fundo de uma imagem. Uma imagem de máscara separada é mencionada por `catalog::MaskPath`. Observe que `layer=0` deve ser especificado explicitamente, caso contrário `op_blur` será aplicado a toda a imagem composta.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
