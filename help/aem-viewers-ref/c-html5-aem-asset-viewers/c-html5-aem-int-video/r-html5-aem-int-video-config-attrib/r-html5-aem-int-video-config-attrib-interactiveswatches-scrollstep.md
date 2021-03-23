---
description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-title: InteractiveSwatches.scrollstep
solution: Experience Manager
title: InteractiveSwatches.scrollstep
uuid: 6f521aa4-9155-4f14-bc89-e7af24af25f0
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '83'
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

