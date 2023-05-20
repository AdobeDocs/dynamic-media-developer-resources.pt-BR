---
description: Ajuste o brilho. Diminui ou aumenta o brilho da imagem.
solution: Experience Manager
title: op_brightness
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

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

Camada. Se aplica à camada atual ou à imagem composta `layer=comp`. Ignorado pelas camadas de efeito. Imagens CMYK ou camadas são convertidas em RGB antes da operação ser aplicada.

## Padrão {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, sem mudança de brilho.

## Exemplo {#section-c25f952f1b77409abb9ccf885862d75c}

Escurecer um pouco o plano de fundo de uma imagem para enfatizar o conteúdo do primeiro plano:

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
