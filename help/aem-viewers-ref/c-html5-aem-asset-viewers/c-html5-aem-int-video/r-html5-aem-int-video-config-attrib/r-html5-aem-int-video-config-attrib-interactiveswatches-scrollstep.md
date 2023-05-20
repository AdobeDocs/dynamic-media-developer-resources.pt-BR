---
title: InteractiveSwatches.scrollstep
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 15bf7af8-428b-4c1c-b7ad-004563347d7c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---

# InteractiveSwatches.scrollstep{#interactiveswatches-scrollstep}

Atributo de configuração para o Visualizador de vídeo interativo.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]scrollstep= *`etapa`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> etapa</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica o número de amostras que devem ser roladas para cada toque do botão de rolagem correspondente. </p> <p>Se o valor especificado for maior que o número de amostras interativas visíveis, cada toque somente rola pelo número de amostras visíveis para evitar a omissão de qualquer amostra. </p> </td> 
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
