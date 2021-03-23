---
description: Ajuste o brilho. Diminui ou aumenta o brilho da imagem.
seo-description: Ajuste o brilho. Diminui ou aumenta o brilho da imagem.
seo-title: op_brightness
solution: Experience Manager
title: op_brightness
uuid: 751ec9e5-4a70-438d-950c-deff4db034b1
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
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

comando Camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. Ignorado por camadas de efeito. Imagens ou camadas CMYK são convertidas em RGB antes da aplicação da operação.

## Padrão {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, sem alteração de brilho.

## Exemplo {#section-c25f952f1b77409abb9ccf885862d75c}

Esmaecer o plano de fundo de uma imagem levemente para enfatizar o conteúdo do primeiro plano:

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
