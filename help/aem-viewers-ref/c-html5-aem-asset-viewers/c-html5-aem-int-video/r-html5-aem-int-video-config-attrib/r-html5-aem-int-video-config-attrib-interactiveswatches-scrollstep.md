---
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
title: InteractiveSwatches.scrollstep
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 1%

---


# InteractiveSwatches.scrollstep{#interactiveswatches-scrollstep}

Atributo de configuração para o Visualizador de vídeo interativo.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]scrollstep= *`step`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> step</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica o número de amostras a serem roladas para cada toque do botão de rolagem correspondente. </p> <p>Se o valor especificado for maior que o número de amostras interativas visíveis, cada toque só rola pelo número de amostras visíveis para evitar a omissão de qualquer amostra. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`3`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
scrollstep=1
```

