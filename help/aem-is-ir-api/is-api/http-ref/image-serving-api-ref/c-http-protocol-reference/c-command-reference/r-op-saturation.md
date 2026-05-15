---
title: op_saturation
description: Ajuste a saturação. Altera a saturação de cada pixel visível da camada ou imagem composta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd71e27e-6ccc-4ade-9bcf-af8e41bcf381
TQID: 'https://experienceleague.adobe.com/lTgjlQNmfVcS1XswABjicGEHjDUO1PVjM7wD1Zi6o2M'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 93
ht-degree: 0%

---

# op_saturation{#op-saturation}

Ajuste a saturação. Altera a saturação de cada pixel visível da camada ou imagem composta.

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste de saturação (-100...+100 int). </p></td> 
 </tr> 
</table>

`op_saturation=-100` elimina totalmente a saturação da imagem.

## Propriedades {#section-9a3cc9ff060049449554dfa69d92fd53}

Camada. Aplica-se à camada atual ou à imagem composta, se `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`, para nenhuma alteração na saturação. As imagens ou camadas CMYK são convertidas em RGB antes da operação ser aplicada.

## Exemplo {#section-033b272f1b7e4efeb94e841fd8095357}

Manipule uma fotografia colorida para obter uma aparência &quot;high-key&quot;:

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
