---
description: A barra de controle é a área retangular que contém e fica atrás de todos os controles de interface disponíveis para o visualizador de vídeo, como o botão reproduzir/pausar, controles de volume e assim por diante.
seo-description: A barra de controle é a área retangular que contém e fica atrás de todos os controles de interface disponíveis para o visualizador de vídeo, como o botão reproduzir/pausar, controles de volume e assim por diante.
seo-title: Barra de controle
solution: Experience Manager
title: Barra de controle
topic: Dynamic Media
uuid: 5686b670-3c8c-4bef-b428-dc468f6ca05d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# Barra de controle{#control-bar}

A barra de controle é a área retangular que contém e fica atrás de todos os controles de interface disponíveis para o visualizador de vídeo, como o botão reproduzir/pausar, controles de volume e assim por diante.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A barra de controle sempre obtém a largura total do visualizador disponível. É possível alterar sua cor, altura e posição vertical por CSS, em relação ao container do visualizador de vídeo.

O seletor de classe CSS a seguir controla a aparência da barra de controle:

```
.s7videoviewer .s7controlbar
```

## Propriedades CSS da barra de controle {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda superior, incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p> Posição a partir da borda inferior, incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura da barra de controle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor do plano de fundo da barra de controle. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Para configurar um visualizador de vídeo com uma barra de controle cinza de 30 pixels de altura e na parte superior do container do visualizador de vídeo.

```
.s7videoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

