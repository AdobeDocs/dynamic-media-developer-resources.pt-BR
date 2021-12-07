---
title: Barra de controle
description: A barra de controle é a área retangular que contém e fica atrás de todos os controles da interface do usuário disponíveis para o visualizador de Vídeo de recorte inteligente, como o botão reproduzir/pausar e os controles de volume.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# Barra de controle{#control-bar}

A barra de controle é a área retangular que contém e fica atrás de todos os controles da interface do usuário disponíveis para o visualizador de Vídeo de recorte inteligente, como o botão reproduzir/pausar e os controles de volume.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A barra de controle sempre obtém a largura total do visualizador disponível. É possível alterar a cor, a altura e a posição vertical por CSS, em relação ao contêiner do visualizador de Vídeo de recorte inteligente.

O seguinte seletor de classe CSS controla a aparência da barra de controle:

```
.s7smartcropvideoviewer .s7controlbar
```

## Propriedades CSS da barra de controle {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda superior, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p> Posição a partir da borda inferior, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura da barra de controle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor do plano de fundo da barra de controle. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Para configurar um visualizador de Vídeo de recorte inteligente com uma barra de controle cinza com 30 pixels de altura e na parte superior do contêiner do visualizador de Vídeo de recorte inteligente.

```
.s7smartcropvideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
