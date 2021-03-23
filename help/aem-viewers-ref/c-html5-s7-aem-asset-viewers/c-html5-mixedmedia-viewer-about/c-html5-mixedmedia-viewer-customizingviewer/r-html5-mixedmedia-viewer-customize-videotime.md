---
description: A hora do vídeo é a exibição numérica que mostra a hora e a duração atuais do vídeo que está sendo reproduzido.
seo-description: A hora do vídeo é a exibição numérica que mostra a hora e a duração atuais do vídeo que está sendo reproduzido.
seo-title: Tempo do vídeo
solution: Experience Manager
title: Tempo do vídeo
uuid: f93e495b-44a1-493c-9bc6-5c088478ddce
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Tempo do vídeo{#video-time}

A hora do vídeo é a exibição numérica que mostra a hora e a duração atuais do vídeo que está sendo reproduzido.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A família, o tamanho e a cor da fonte da hora do vídeo estão entre as propriedades que o CSS pode controlar. Ele também pode ser posicionado, em relação à barra de controle que a contém, por CSS.

A aparência da hora de vídeo é controlada pelo seguinte seletor de classe CSS:

```
.s7mixedmediaviewer .s7videotime
```

## Propriedades CSS do tempo de vídeo {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda superior, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda direita, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> A largura do controle de tempo do vídeo. Essa propriedade é necessária para que o Internet Explorer 8 ou superior funcione corretamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>A família de fontes a ser usada para o texto de exibição de tempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte  </span> </p> </td> 
   <td colname="col2"> <p>O tamanho da fonte a ser usado para o texto de exibição de tempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>A cor da fonte a ser usada para o texto de exibição de tempo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Defina o tempo do vídeo como cinza claro (hexadecimal `#BBBBBB`), dimensionado em 12 pixels, posicionado 15 pixels da parte superior da barra de controle e 80 pixels das margens direitas da barra de controle.

```
.s7mixedmediaviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```

