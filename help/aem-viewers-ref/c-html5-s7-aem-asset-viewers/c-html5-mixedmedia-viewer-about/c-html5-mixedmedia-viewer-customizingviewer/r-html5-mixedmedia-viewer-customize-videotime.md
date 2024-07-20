---
title: Tempo do vídeo
description: A hora do vídeo é a exibição numérica que mostra a hora e a duração atuais do vídeo em reprodução no momento.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 5efae314-5f37-4afc-9b9e-3108a8529e50
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# Tempo do vídeo{#video-time}

A hora do vídeo é a exibição numérica que mostra a hora e a duração atuais do vídeo em reprodução no momento.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A família da fonte de tempo do vídeo, o tamanho da fonte e a cor da fonte estão entre as propriedades que o CSS pode controlar. Ele também pode ser posicionado, em relação à barra de controle que o contém, pelo CSS.

A aparência do tempo de vídeo é controlada com o seguinte seletor de classe CSS:

```
.s7mixedmediaviewer .s7videotime
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
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>A família da fonte a ser usada para o texto de exibição de hora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>O tamanho da fonte a ser usada para o texto de exibição de tempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>A cor da fonte a ser usada para o texto de exibição da hora. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Defina o tempo do vídeo como cinza-claro (hexadecimal `#BBBBBB`), dimensionado a 12 pixels, posicionado a 15 pixels da parte superior da barra de controle e a 80 pixels das bordas direitas da barra de controle.

```
.s7mixedmediaviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
