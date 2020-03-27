---
description: nulo
seo-description: nulo
seo-title: PageView.fmt
solution: Experience Manager
title: PageView.fmt
topic: Dynamic media
uuid: 302e20bf-d398-45de-98a5-58b9edde48f3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.fmt{#pageview-fmt}

`[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alfa|gif|gif-alfa</span> </p> </td> 
   <td colname="col2"> <p> Especifica o formato de imagem que o componente usa para carregar imagens do Servidor de imagens. Se o formato especificado terminar com <span class="codeph"> -alfa</span>, o componente renderizará as imagens como conteúdo transparente. Para todos os outros formatos de imagem, o componente trata as imagens como opacas. O componente tem um fundo branco por padrão. Portanto, para torná-la transparente, defina a propriedade CSS de cor <span class="codeph"> de fundo como</span> transparente <span class="codeph"></span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-12a6fb2fcbc1476b95bd53ce880dc185}

Opcional.

## Padrão {#section-4b6a350501124ffa9a6b1b71b32eff5d}

`jpeg`

## Example {#section-7de29e43bb3640e4aa1f8984b4afddad}

`fmt=png-alpha`
