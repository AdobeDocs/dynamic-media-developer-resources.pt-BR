---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
topic: Dynamic Media
uuid: 6fa79ce2-5191-4282-acee-5c6caad24fba
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 1%

---


# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> A string de comando do Servidor de imagens que é aplicada a todas as amostras. Se for especificado no URL, certifique-se de que você codifica por HTTP todas as ocorrências de <span class="codeph"> &amp;</span> e <span class="codeph"> =</span> como <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>, respectivamente. </p> <p> <p>Observação:  Comandos de manipulação de dimensionamento de imagem não são suportados. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

Nenhum.

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

Quando especificado no URL do visualizador.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Quando especificado nos dados de configuração.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
