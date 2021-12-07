---
title: videoServerUrl
description: comando URL para o Visualizador de vídeo de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 1%

---

# videoServerUrl{#videoserverurl}

comando URL para o Visualizador de vídeo de recorte inteligente.

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> O caminho raiz do servidor de vídeo. Se nenhum domínio for especificado, o domínio do qual a página é disponibilizada será aplicado. A resolução de caminho URI padrão se aplica. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional. Não é necessário para o uso padrão de SaaS.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
