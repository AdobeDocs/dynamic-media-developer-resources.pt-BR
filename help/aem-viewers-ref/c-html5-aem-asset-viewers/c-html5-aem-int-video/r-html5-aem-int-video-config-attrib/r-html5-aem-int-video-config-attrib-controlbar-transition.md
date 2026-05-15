---
title: ControlBar.transition
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
TQID: 'https://experienceleague.adobe.com/mTLUrXKC7m8pIC5Sqoor0M-N-vmwlZzM9WxnvwzlqD8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 0%

---

# ControlBar.transition{#controlbar-transition}

Atributo de configuração para o Visualizador de vídeo interativo.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhuma|desaparecimento</span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de efeito que é usado para mostrar/ocultar a barra de controle e seu conteúdo. </p> <p>Defina como <span class="codeph"> none</span> para mostrar/ocultar instantâneos. </p> <p>Defina como <span class="codeph"> fade</span> para fornecer um efeito de desaparecimento/aparecimento gradual. Não suportado no Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o tempo em segundos entre o último evento de mouse/toque registrado pela barra de controle e a barra de controle de tempo fica oculta. Se definido como <span class="codeph"> -1</span>, o componente nunca acionará seu efeito de ocultação automática e, portanto, sempre permanecerá visível na tela. </p> </td> 
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
