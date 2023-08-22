---
title: op_saturation
description: Ajuste a saturação. Altera a saturação de cada pixel visível da camada ou imagem composta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd71e27e-6ccc-4ade-9bcf-af8e41bcf381
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '90'
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

Camada. Se aplica à camada atual ou à imagem composta `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`, para nenhuma alteração na saturação. Imagens CMYK ou camadas são convertidas em RGB antes da operação ser aplicada.

## Exemplo {#section-033b272f1b7e4efeb94e841fd8095357}

Manipule uma fotografia colorida para obter uma aparência de &quot;alta definição&quot;:

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
