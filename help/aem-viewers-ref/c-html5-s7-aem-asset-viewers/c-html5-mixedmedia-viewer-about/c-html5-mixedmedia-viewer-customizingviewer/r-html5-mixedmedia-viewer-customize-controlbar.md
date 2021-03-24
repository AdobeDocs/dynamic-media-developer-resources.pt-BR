---
description: A barra de controle é a área retangular que contém e fica atrás de todos os controles da interface de usuário disponíveis para o visualizador de vídeo, como o botão Reproduzir/pausar, controles de volume e assim por diante.
solution: Experience Manager
title: Barra de controle
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---


# Barra de controle{#control-bar}

A barra de controle é a área retangular que contém e fica atrás de todos os controles da interface de usuário disponíveis para o visualizador de vídeo, como o botão Reproduzir/pausar, controles de volume e assim por diante.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A barra de controle sempre obtém a largura total do visualizador disponível. É possível alterar a cor, a altura e a posição vertical por CSS, em relação ao contêiner do visualizador de vídeo.

O seguinte seletor de classe CSS controla a aparência da barra de controle:

```
.s7mixedmediaviewer .s7controlbar
```

## Propriedades CSS da barra de controle {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura da barra de controle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
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

