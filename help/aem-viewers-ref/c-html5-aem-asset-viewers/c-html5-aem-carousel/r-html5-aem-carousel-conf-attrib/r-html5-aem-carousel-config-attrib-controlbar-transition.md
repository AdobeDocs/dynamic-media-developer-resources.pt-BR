---
description: Atributo de configuração para o Visualizador de carrossel.
seo-description: Atributo de configuração para o Visualizador de carrossel.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
uuid: 80053511-f0e2-49f6-a1db-cd96c7788703
feature: Dynamic Media Classic,Visualizadores,SDK/API,Banners em carrossel
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# ControlBar.transition{#controlbar-transition}

Atributo de configuração para o Visualizador de carrossel.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|desaparecer</span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de efeito usado para mostrar ou ocultar a barra de controle e seu conteúdo. </p> <p>Defina como <span class="codeph"> nenhum</span> para mostrar/ocultar instantaneamente. </p> <p>Defina como <span class="codeph"> fade</span> para fornecer um efeito de entrada/saída gradual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o tempo em segundos entre o último evento de mouse/toque registrado pela barra de controle e a barra de controle de tempo oculta. </p> <p>Se definido como <span class="codeph"> -1</span> o componente nunca aciona seu efeito de ocultação automática e, portanto, sempre fica visível na tela. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p> Define a duração da animação de entrada/saída do fade em segundos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional. Esse comando é ignorado em dispositivos de toque, onde a ocultação automática da barra de controle está desativada.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

