---
description: PageView.fmt
solution: Experience Manager
title: PageView.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 690aed79-c242-402d-86c0-470a91fbb034
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---

# PageView.fmt{#pageview-fmt}

[!DNL `[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Especifica o formato de imagem que o componente usa para carregar imagens do Servidor de imagens. Se o formato especificado termina com <span class="codeph"> -alpha</span>, o componente renderiza imagens como conteúdo transparente. Para todos os outros formatos de imagem, o componente trata as imagens como opacas. Por padrão, o componente possui um plano de fundo branco. Portanto, para torná-lo transparente, defina a propriedade CSS <span class="codeph"> background-color</span> como <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-12a6fb2fcbc1476b95bd53ce880dc185}

Opcional.

## Padrão {#section-4b6a350501124ffa9a6b1b71b32eff5d}

[!DNL `jpeg`]

## Exemplo {#section-7de29e43bb3640e4aa1f8984b4afddad}

[!DNL `fmt=png-alpha`]
