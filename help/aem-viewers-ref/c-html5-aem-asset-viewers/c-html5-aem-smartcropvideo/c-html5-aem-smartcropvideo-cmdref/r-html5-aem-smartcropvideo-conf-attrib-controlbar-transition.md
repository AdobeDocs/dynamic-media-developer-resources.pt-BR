---
description: Atributo de configuração para o Visualizador de vídeo de recorte inteligente.
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 133717c7-38d9-47b6-86bb-e23ebd8f147a
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# ControlBar.transition{#controlbar-transition}

Atributo de configuração para o Visualizador de vídeo de recorte inteligente.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|desaparecer</span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de efeito usado para mostrar ou ocultar a barra de controle e seu conteúdo. </p> <p>Use <span class="codeph"> nenhum</span> para show e ocultação instantâneos. Use <span class="codeph"> desaparecer</span> para proporcionar um efeito gradual de atenuação e desvanecimento. </p> <p>O Fade não é compatível com o Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica o tempo em segundos entre o último evento mouse/toque que a barra de controle registra e o tempo de controle barra oculta. </p> <p> Se estiver definido como <span class="codeph"> -1</span> o componente nunca aciona seu efeito de ocultação automática e sempre fica visível na tela. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>Define a duração do esmaecimento e do esmaecimento da animação, em segundos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```
