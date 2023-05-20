---
title: Barra de controle
description: A barra de controle é a área retangular que contém e fica atrás de todos os controles da interface do usuário disponíveis para o visualizador de vídeo, como o botão Reproduzir/Pausar, controles de volume e assim por diante.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f0de655c-36f0-4ed4-806c-d486eed2201b
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Barra de controle{#control-bar}

A barra de controle é a área retangular que contém e fica atrás de todos os controles da interface do usuário disponíveis para o visualizador de vídeo, como o botão Reproduzir/Pausar, controles de volume e assim por diante.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A barra de controle sempre ocupa toda a largura disponível do visualizador. É possível alterar a cor, a altura e a posição vertical por CSS, em relação ao contêiner do visualizador de vídeo.

O seletor de classe CSS a seguir controla a aparência da barra de controle:

```
.s7mixedmediaviewer .s7controlbar
```

## Propriedades CSS da barra de controle {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura da barra de controle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Cor do plano de fundo da barra de controle. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Para configurar um visualizador de mídia mista com uma barra de controle cinza com 30 pixels de altura.

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
