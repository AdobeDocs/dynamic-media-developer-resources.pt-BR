---
title: PanoramicView.iscommand
description: Atributo de configuração para Visualizador panorâmico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 1%

---

# PanoramicView.iscommand{#panoramicview-iscommand}

Atributo de configuração para Visualizador panorâmico.

` [PanoramicView.|<containerId>_panoramicView.]iscommand=isCommand `

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> A string de comando Exibição de imagem que é aplicada à imagem.  Se ele for especificado no URL, certifique-se de codificar HTTP todas as ocorrências de <span class="codeph"> &amp;</span> e <span class="codeph"> =</span> as <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

Sem padrão.

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Quando especificado no URL do visualizador.

```
iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000
```

Quando especificado nos dados de configuração.

```
iscommand=op_sharpen=1&op_colorize=0xff0000
```
