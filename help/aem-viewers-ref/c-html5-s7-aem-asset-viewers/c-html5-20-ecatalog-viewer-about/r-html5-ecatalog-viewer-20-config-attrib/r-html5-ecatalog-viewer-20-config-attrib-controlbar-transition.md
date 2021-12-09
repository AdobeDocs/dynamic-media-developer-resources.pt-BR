---
title: ControlBar.transition
description: Especifica o tipo de efeito usado para mostrar ou ocultar a barra de controle e seu conteúdo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: abe8affb-cbcd-4072-b2ed-91a398b1d678
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|desaparecer </span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de efeito usado para mostrar ou ocultar a barra de controle e seu conteúdo. Use <span class="codeph"> nenhum </span> para espetáculos e esconderijos instantâneos; <span class="codeph"> desaparecer </span> O fornece um efeito gradual de inatividade e desvanecimento (não compatível com o Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica o tempo em segundos entre o último evento mouse/toque que a barra de controle registra e o ocultamento da barra de controle de tempo. </p> <p> Se estiver definido como <span class="codeph"> -1 </span>, o componente nunca aciona seu efeito de ocultação automática e sempre fica visível na tela. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration </span> </span> </p> </td> 
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
