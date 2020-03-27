---
description: Atributo de configuração para o Visualizador do carrossel.
seo-description: Atributo de configuração para o Visualizador do carrossel.
seo-title: ControlBar.transição
solution: Experience Manager
title: ControlBar.transição
topic: Dynamic media
uuid: 80053511-f0e2-49f6-a1db-cd96c7788703
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.transição{#controlbar-transition}

Atributo de configuração para o Visualizador do carrossel.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *``*[, *`retardo`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de efeito usado para mostrar ou ocultar a barra de controle e seu conteúdo. </p> <p>Defina como <span class="codeph"> nenhum</span> para mostrar/ocultar instantaneamente. </p> <p>Definido para <span class="codeph"> desaparecer</span> para fornecer um efeito gradual de entrada/saída. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o tempo em segundos entre o último evento mouse/toque registrado pela barra de controle e o tempo de ocultação da barra de controle. </p> <p>Se definido como <span class="codeph"> -1</span> , o componente nunca aciona seu efeito de ocultação automática e, portanto, sempre fica visível na tela. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duração</span></span> </p> </td> 
   <td colname="col2"> <p> Define a duração da animação de entrada/saída gradual em segundos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional. Esse comando é ignorado em dispositivos de toque nos quais a barra de controle oculta automaticamente está desativada.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

