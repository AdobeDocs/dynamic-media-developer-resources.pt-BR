---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic Media
uuid: 803df8d4-6fb9-49ef-a097-c883d4115fad
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---


# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`retardo`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de efeito usado para mostrar ou ocultar a barra de controle e seu conteúdo. </p> <p>Use <span class="codeph"> none</span> para mostrar e ocultar instantaneamente. Use <span class="codeph"> fade</span> para fornecer um efeito gradual de aparecimento e desaparecimento gradual. </p> <p>O Fade não é suportado no Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica o tempo em segundos entre o último evento mouse/toque registrado pela barra de controle e o tempo de ocultação da barra de controle. </p> <p> Se definido como <span class="codeph"> -1</span> o componente nunca aciona seu efeito de ocultação automática e sempre fica visível na tela. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duração</span> </span> </p> </td> 
   <td colname="col2"> <p>Define a duração da animação de aparecimento e desaparecimento gradual, em segundos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
