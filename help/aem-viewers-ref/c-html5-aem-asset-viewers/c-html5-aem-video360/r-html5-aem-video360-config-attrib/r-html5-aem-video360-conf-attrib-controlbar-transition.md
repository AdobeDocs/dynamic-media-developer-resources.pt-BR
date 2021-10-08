---
title: ControlBar.transition
description: Atributo de configuração para o visualizador do Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 950b1230-5c4b-4222-87e2-d069287fc3ff
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# ControlBar.transition{#controlbar-transition}

Atributo de configuração para o visualizador do Video360.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|desaparecer</span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de efeito usado para mostrar ou ocultar a barra de controle e seu conteúdo. </p> <p>Use <span class="codeph"> none</span> para mostrar e ocultar instantaneamente. Use <span class="codeph"> fade</span> para fornecer um efeito de fade in e fade out gradual. </p> <p>O Fade não é compatível com o Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica o tempo em segundos entre o último evento mouse/toque registrado pela barra de controle e o tempo de ocultação da barra de controle. </p> <p> Se definido como <span class="codeph"> -1</span>, o componente nunca acionará seu efeito de ocultação automática e sempre permanecerá visível na tela. </p> </td> 
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
