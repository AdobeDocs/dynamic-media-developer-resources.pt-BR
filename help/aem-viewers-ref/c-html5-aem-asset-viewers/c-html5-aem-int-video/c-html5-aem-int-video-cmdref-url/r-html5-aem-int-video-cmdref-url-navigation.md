---
description: comando URL para Visualizador de vídeo interativo.
seo-description: comando URL para Visualizador de vídeo interativo.
seo-title: navegação
solution: Experience Manager
title: navegação
uuid: eecc7458-153c-4f36-b29e-97451f275c0c
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 1%

---


# navegação{#navigation}

comando URL para Visualizador de vídeo interativo.

` navigation= *`arquivo`*`

O visualizador oferece suporte à navegação de capítulo de vídeo por meio de arquivos WebVTT hospedados. Os operadores de posicionamento de sinalização não são compatíveis.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> arquivo</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica um URL ou caminho para o conteúdo de navegação da WebVTT. O Image Serving deve hospedar o arquivo WebVTT. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

Nenhum.

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
navigation=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.navigation.vtt,1
```

