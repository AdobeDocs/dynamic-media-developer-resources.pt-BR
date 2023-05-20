---
title: ControlBar.transition
description: Atributo de configuração para o Visualizador do carrossel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# ControlBar.transition{#controlbar-transition}

Atributo de configuração para o Visualizador do carrossel.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *`delaytohide`*[, *`duração`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|esmaecer</span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de efeito usado para mostrar ou ocultar a barra de controle e seu conteúdo. </p> <p>Defina como <span class="codeph"> nenhum</span> para mostrar/ocultar instantâneos. </p> <p>Defina como <span class="codeph"> fade</span> para proporcionar um efeito de desaparecimento/aparecimento gradual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o tempo em segundos entre o último evento de mouse/toque registrado pela barra de controle e a barra de controle de tempo fica oculta. </p> <p>Se definida como <span class="codeph"> -1</span> o componente nunca aciona o efeito de ocultação automática e, portanto, sempre permanece visível na tela. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duração</span></span> </p> </td> 
   <td colname="col2"> <p> Define a duração da animação de aparecimento/desaparecimento gradual em segundos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional. Esse comando é ignorado em dispositivos de toque nos quais a ocultação automática da barra de controle está desativada.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
