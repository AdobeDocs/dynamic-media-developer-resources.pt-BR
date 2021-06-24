---
description: comando URL para Visualizador de vídeo.
solution: Experience Manager
title: videoServerUrl
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Developer,Business Practitioner
exl-id: 945c32e0-a67b-4c27-b661-26510615d757
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 1%

---

# videoServerUrl{#videoserverurl}

comando URL para Visualizador de vídeo.

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
