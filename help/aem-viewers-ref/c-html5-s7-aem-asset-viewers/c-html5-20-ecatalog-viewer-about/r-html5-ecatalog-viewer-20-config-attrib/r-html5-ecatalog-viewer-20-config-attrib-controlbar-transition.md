---
description: nulo
seo-description: nulo
seo-title: ControlBar.transição
solution: Experience Manager
title: ControlBar.transição
topic: Dynamic media
uuid: e029173b-c004-4be8-b304-d6e2183314ad
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.transição{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`retardo`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade </span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de efeito usado para mostrar ou ocultar a barra de controle e seu conteúdo. Usar <span class="codeph"> nenhum </span> para mostrar e ocultar instantaneamente; O <span class="codeph"> desaparecimento gradual </span> fornece um efeito gradual de aparecimento e desaparecimento gradual (não suportado no Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o tempo em segundos entre o último evento mouse/toque registrado pela barra de controle e o tempo de ocultação da barra de controle. </p> <p> Se definido como <span class="codeph"> -1, </span> o componente nunca ativa seu efeito de ocultação automática e sempre fica visível na tela. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duração </span></span> </p> </td> 
   <td colname="col2"> <p> Define a duração da animação de aparecimento e desaparecimento gradual, em segundos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional. Esse comando é ignorado em dispositivos de toque, onde a barra de controle oculta automaticamente está desativada.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
