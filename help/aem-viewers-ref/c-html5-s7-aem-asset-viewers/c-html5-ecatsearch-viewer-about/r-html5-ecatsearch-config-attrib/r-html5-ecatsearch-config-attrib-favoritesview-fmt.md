---
description: FavoritesView.fmt
solution: Experience Manager
title: FavoritesView.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 9ec5ed03-1d8f-4e67-a9a3-bdf160b105c5
TQID: 'https://experienceleague.adobe.com/1FCwR44MoYdknONSzCGj-dMTRjoukHBEOX5IA568H5Y'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 72
ht-degree: 0%

---

# FavoritesView.fmt{#favoritesview-fmt}

[!DNL `[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Especifica o formato de imagem a ser usado pelo componente para carregar imagens do Servidor de imagens. O formato é qualquer valor suportado pelo Servidor de imagens e pelo navegador cliente. </p> <p>Se o formato de imagem terminar com <span class="codeph"> -alpha</span>, o componente renderiza as imagens como conteúdo transparente. Para todos os outros valores de formato de imagem, o componente trata as imagens como opacas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
