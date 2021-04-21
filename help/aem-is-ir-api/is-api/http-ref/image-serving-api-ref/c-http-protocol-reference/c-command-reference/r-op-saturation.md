---
description: Ajuste a saturação. Altera a saturação de cada pixel visível da camada ou imagem composta.
solution: Experience Manager
title: op_saturation
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '98'
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

`op_saturation=-100` dessatura totalmente a imagem.

## Propriedades {#section-9a3cc9ff060049449554dfa69d92fd53}

comando Camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. Ignorado por camadas de efeito.

## Padrão {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`, sem alteração na saturação. Imagens ou camadas CMYK são convertidas em RGB antes da aplicação da operação.

## Exemplo {#section-033b272f1b7e4efeb94e841fd8095357}

Manipule uma fotografia colorida para obter uma aparência &quot;de alta definição&quot;:

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
