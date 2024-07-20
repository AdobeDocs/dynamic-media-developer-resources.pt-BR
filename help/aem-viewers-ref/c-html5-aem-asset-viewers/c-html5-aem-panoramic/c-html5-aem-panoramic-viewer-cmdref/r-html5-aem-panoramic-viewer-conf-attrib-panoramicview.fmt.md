---
title: PanoramicView.fmt
description: Especifica o formato de imagem a ser usado pelo componente para carregar imagens do Servidor de imagens.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# PanoramicView.fmt{#panoramicview-fmt}

Especifica o formato de imagem a ser usado pelo componente para carregar imagens do Servidor de imagens. Se o formato especificado termina com &quot;-alpha&quot;, o componente renderiza as imagens como transparentes. Para todos os outros formatos de imagem, o componente trata as imagens como opacas. O componente tem um plano de fundo transparente por padrão. Portanto, para torná-lo opaco, defina a propriedade CSS `background-color` como `desired_color`

`[PanoramicView.|<containerId>_panoramicView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha </span> </p> </td> 
   <td colname="col2"> <p> Especifica o formato de imagem a ser usado pelo componente para carregar imagens do Servidor de imagens. Se o formato especificado terminar com "-alpha", o componente renderiza imagens como conteúdo transparente; para todos os outros formatos de imagem, o componente trata as imagens como opacas. O componente tem um plano de fundo transparente por padrão. Portanto, para opaco, defina a propriedade CSS background-color para a cor desejada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
