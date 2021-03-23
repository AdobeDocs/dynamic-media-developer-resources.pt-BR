---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
uuid: b5dfb326-fbd8-4220-a44c-0d4f80b2a8fa
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '73'
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

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Nenhum.

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

Quando especificado no URL do visualizador.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Quando especificado nos dados de configuração.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
