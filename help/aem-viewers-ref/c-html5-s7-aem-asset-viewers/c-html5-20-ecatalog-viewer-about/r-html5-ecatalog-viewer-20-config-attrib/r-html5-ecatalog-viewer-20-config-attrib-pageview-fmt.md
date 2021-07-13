---
description: PageView.fmt
solution: Experience Manager
title: PageView.fmt
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Developer,User
exl-id: 07aec907-fb9d-41c8-9f32-a4886605db35
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---

# PageView.fmt{#pageview-fmt}

`[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Especifica o formato de imagem que o componente usa para carregar imagens do Servidor de imagem. Se o formato especificado terminar com <span class="codeph"> -alpha</span>, o componente renderizará as imagens como conteúdo transparente. Para todos os outros formatos de imagem, o componente trata as imagens como opacas. Por padrão, o componente tem um fundo branco. Portanto, para torná-lo transparente, defina a propriedade CSS <span class="codeph"> background-color</span> para <span class="codeph"> transparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-12a6fb2fcbc1476b95bd53ce880dc185}

Opcional.

## Padrão {#section-4b6a350501124ffa9a6b1b71b32eff5d}

`jpeg`

## Exemplo {#section-7de29e43bb3640e4aa1f8984b4afddad}

`fmt=png-alpha`
