---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flyout
role: Developer,Business Practitioner
exl-id: ed587082-3306-4914-916f-db37a823e199
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 1%

---

# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> A string de comando Image Serving que é aplicada a todas as amostras. Se estiver especificado no URL, certifique-se de codificar HTTP todas as ocorrências de <span class="codeph"> &amp;</span> e <span class="codeph"> =</span> como <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>, respectivamente. </p> <p> <p>Observação:  Comandos de manipulação de dimensionamento de imagem não são suportados. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

Nenhum.

## Exemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

Quando especificado no URL do visualizador:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Quando especificado nos dados de configuração:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
