---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
uuid: e029173b-c004-4be8-b304-d6e2183314ad
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|desaparecer  </span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de efeito usado para mostrar ou ocultar a barra de controle e seu conteúdo. Use <span class="codeph"> nenhum </span> para mostrar e ocultar instantaneamente; <span class="codeph"> fade </span> fornece um efeito de fade in e fade out gradual (não compatível com o Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica o tempo em segundos entre o último evento mouse/toque que a barra de controle registra e o tempo de controle barra oculta. </p> <p> Se definido como <span class="codeph"> -1 </span> o componente nunca aciona seu efeito de ocultação automática e sempre fica visível na tela. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration  </span> </span> </p> </td> 
   <td colname="col2"> <p> Define a duração do esmaecimento e do esmaecimento da animação, em segundos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional. Esse comando é ignorado em dispositivos de toque, onde a ocultação automática da barra de controle está desativada.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
