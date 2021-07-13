---
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
title: CallToAction.fmt
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Developer,User
exl-id: 38ca592f-329c-4fd4-8dbc-a49000663e55
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 1%

---

# CallToAction.fmt{#calltoaction-fmt}

Atributo de configuração para o Visualizador de vídeo interativo.

`[CallToAction.|<containerId>_callToAction.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Especifica o formato de imagem que o componente usa para carregar imagens do Servidor de imagem. </p> <p>Se o formato especificado terminar com "<span class="codeph"> -alpha</span>", o componente renderizará as imagens como conteúdo transparente. Para todos os outros formatos de imagem, o componente trata as imagens como opacas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
fmt=png-alpha
```
