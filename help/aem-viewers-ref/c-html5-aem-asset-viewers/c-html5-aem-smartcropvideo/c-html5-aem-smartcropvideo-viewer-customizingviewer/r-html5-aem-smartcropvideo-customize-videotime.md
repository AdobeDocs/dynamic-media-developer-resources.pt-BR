---
title: Tempo do vídeo
description: A hora do vídeo é a exibição numérica que mostra a hora e a duração atuais do vídeo em reprodução no momento.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 0ef09f06-c2d5-4c84-8ff9-4e94e9e54d40
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Tempo do vídeo{#video-time}

A hora do vídeo é a exibição numérica que mostra a hora e a duração atuais do vídeo em reprodução no momento.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A família da fonte de tempo do vídeo, o tamanho da fonte e a cor da fonte estão entre as propriedades que o CSS pode controlar. Ele também pode ser posicionado, em relação à barra de controle que o contém, pelo CSS.

A aparência do tempo de vídeo é controlada com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7videotime
```

## Propriedades CSS do tempo de vídeo {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda superior, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> direita </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda direita, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p> A largura do controle de tempo do vídeo. Esta propriedade é necessária para que o Internet Explorer 8 ou posterior funcione corretamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>A família da fonte a ser usada para o texto de exibição de hora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>O tamanho da fonte a ser usada para o texto de exibição de tempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>A cor da fonte a ser usada para o texto de exibição da hora. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Defina a hora do vídeo como cinza-claro (hexadecimal) `#BBBBBB`), dimensionado em 12 pixels, posicionado a 15 pixels da parte superior da barra de controle e a 80 pixels das bordas direitas da barra de controle.

```
.s7smartcropvideoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
