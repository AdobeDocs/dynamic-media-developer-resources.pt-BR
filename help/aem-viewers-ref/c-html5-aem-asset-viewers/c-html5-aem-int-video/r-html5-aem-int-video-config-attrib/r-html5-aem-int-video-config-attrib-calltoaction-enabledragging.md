---
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
title: CallToAction.enabledragging
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---


# CallToAction.enabledragging{#calltoaction-enabledragging}

Atributo de configuração para o Visualizador de vídeo interativo.

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Ativa ou desativa a capacidade de um usuário rolar as miniaturas com um mouse ou usando gestos de toque. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td colname="col2"> <p> Está no intervalo <span class="codeph"> 0-1 </span> e é um valor percentual para o movimento na direção errada da velocidade real. </p> <p>Se definido como <span class="codeph"> 1 </span>, ele se move com o mouse. </p> <p>Se definido como <span class="codeph"> 0 </span>, não permite que você se mova na direção errada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```

