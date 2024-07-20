---
title: Área do visualizador principal
description: A área de visualização principal é ocupada pelo vídeo. Normalmente, ele é configurado para se ajustar à tela do dispositivo disponível quando nenhum tamanho é especificado.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 7d1379c1-7746-4f61-92df-e8ac4ab7d506
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Área do visualizador principal{#main-viewer-area}

A área de visualização principal é ocupada pelo vídeo. Normalmente, ele é configurado para se ajustar à tela do dispositivo disponível quando nenhum tamanho é especificado.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

O seletor de classe CSS a seguir controla a aparência da área de visualização:

```
.s7videoviewer 
```

## Propriedades CSS da área do visualizador principal {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor de fundo em formato hexadecimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Para configurar um visualizador de vídeo com um plano de fundo branco (#FFFFFF) e definir seu tamanho como 512 x 288 pixels:

```
.s7videoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
