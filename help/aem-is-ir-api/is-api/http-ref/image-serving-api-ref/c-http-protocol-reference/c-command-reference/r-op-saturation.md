---
description: Ajuste a saturação. Altera a saturação de cada pixel visível da camada ou imagem composta.
seo-description: Ajuste a saturação. Altera a saturação de cada pixel visível da camada ou imagem composta.
seo-title: op_saturation
solution: Experience Manager
title: op_saturation
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5e987841-0c3b-4f68-96b1-fad8757f3402
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '107'
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

`op_saturation=-100` dessatura total da imagem.

## Propriedades {#section-9a3cc9ff060049449554dfa69d92fd53}

comando Camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`, sem alteração na saturação. As imagens ou camadas CMYK são convertidas em RGB antes da operação ser aplicada.

## Exemplo {#section-033b272f1b7e4efeb94e841fd8095357}

Manipule uma fotografia colorida para obter uma aparência &quot;chave&quot;:

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
