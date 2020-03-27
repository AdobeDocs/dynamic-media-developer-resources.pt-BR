---
description: Ajuste o brilho. Diminui ou aumenta o brilho da imagem.
seo-description: Ajuste o brilho. Diminui ou aumenta o brilho da imagem.
seo-title: op_brightness
solution: Experience Manager
title: op_brightness
topic: Scene7 Image Serving - Image Rendering API
uuid: 751ec9e5-4a70-438d-950c-deff4db034b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_brightness{#op-brightness}

Ajuste o brilho. Diminui ou aumenta o brilho da imagem.

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste de brilho (-100...+100 int). </p></td> 
 </tr> 
</table>

## Propriedades {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

comando Camada. Aplica-se à camada atual ou à imagem composta, se `layer=comp`. Ignorado pelas camadas de efeito. As imagens ou camadas CMYK são convertidas em RGB antes da operação ser aplicada.

## Padrão {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, sem alteração de brilho.

## Example {#section-c25f952f1b77409abb9ccf885862d75c}

Escureça levemente o plano de fundo de uma imagem para enfatizar o conteúdo do primeiro plano:

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
