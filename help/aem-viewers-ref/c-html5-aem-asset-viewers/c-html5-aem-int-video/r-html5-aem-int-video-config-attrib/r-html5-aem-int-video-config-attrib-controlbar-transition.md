---
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# ControlBar.transition{#controlbar-transition}

Atributo de configuração para o Visualizador de vídeo interativo.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|desaparecer</span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de efeito que será usado para mostrar/ocultar a barra de controle e seu conteúdo. </p> <p>Defina como <span class="codeph"> nenhum</span> para mostrar/ocultar instantaneamente. </p> <p>Defina como <span class="codeph"> fade</span> para fornecer um efeito de entrada/saída gradual. Não suportado no Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o tempo em segundos entre o último evento de mouse/toque registrado pela barra de controle e a barra de controle de tempo oculta. Se definido como <span class="codeph"> -1</span> o componente nunca aciona seu efeito de ocultação automática e, portanto, sempre fica visível na tela. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p> Define a duração da animação de entrada/saída do fade, em segundos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
