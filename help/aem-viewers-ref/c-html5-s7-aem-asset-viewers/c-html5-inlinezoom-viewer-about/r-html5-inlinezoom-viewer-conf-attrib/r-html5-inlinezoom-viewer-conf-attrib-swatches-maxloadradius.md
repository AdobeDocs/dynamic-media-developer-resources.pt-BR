---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom em linha
role: Developer,User
exl-id: 574cb37c-009a-43c7-ae55-8b26c0c096c5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 1%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o comportamento de pré-carregamento do componente. Quando definido como <span class="codeph"> -1</span> todas as amostras serão carregadas simultaneamente quando o componente for inicializado ou o ativo for alterado. Quando definido como <span class="codeph"> 0</span>, apenas as amostras visíveis são carregadas. </p> <p><span class="codeph"> <span class="varname"> </span></span> pré-carregamento define quantas linhas/colunas invisíveis em torno da área visível serão pré-carregadas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Padrão {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1`

## Exemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`maxloadradius=-1`
