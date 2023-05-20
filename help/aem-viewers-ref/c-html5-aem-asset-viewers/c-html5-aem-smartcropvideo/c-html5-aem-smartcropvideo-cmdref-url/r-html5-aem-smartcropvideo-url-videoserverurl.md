---
title: videoServerUrl
description: Comando de URL para o Visualizador de Corte inteligente de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 9bd37d2c-c7ec-4f58-8328-45c0a156f330
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 0%

---

# videoServerUrl{#videoserverurl}

Comando de URL para o Visualizador de Corte inteligente de vídeo.

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> O caminho raiz do servidor de vídeo. Se nenhum domínio for especificado, o domínio que fornece a página será aplicado. É aplicada a resolução de caminho URI padrão. </p> </td> 
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
