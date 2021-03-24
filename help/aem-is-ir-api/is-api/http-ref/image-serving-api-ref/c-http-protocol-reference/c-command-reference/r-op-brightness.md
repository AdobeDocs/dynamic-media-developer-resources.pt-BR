---
description: Ajuste o brilho. Diminui ou aumenta o brilho da imagem.
solution: Experience Manager
title: op_brightness
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
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
