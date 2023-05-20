---
title: ControlBar.transition
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# ControlBar.transition{#controlbar-transition}

Atributo de configuração para o Visualizador de vídeo interativo.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duração`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|esmaecer</span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de efeito que é usado para mostrar/ocultar a barra de controle e seu conteúdo. </p> <p>Defina como <span class="codeph"> nenhum</span> para mostrar/ocultar instantâneos. </p> <p>Defina como <span class="codeph"> fade</span> para proporcionar um efeito de desaparecimento/aparecimento gradual. Não suportado no Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o tempo em segundos entre o último evento de mouse/toque registrado pela barra de controle e a barra de controle de tempo fica oculta. Se definida como <span class="codeph"> -1</span> o componente nunca aciona o efeito de ocultação automática e, portanto, sempre permanece visível na tela. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duração</span></span> </p> </td> 
   <td colname="col2"> <p> Define a duração da animação de aparecimento/desaparecimento, em segundos. </p> </td> 
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
