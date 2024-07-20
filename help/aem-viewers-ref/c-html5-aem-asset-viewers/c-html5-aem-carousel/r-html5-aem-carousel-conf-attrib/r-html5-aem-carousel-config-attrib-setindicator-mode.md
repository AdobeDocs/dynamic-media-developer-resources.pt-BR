---
title: SetIndicator.mode
description: SetIndicator.mode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numérico|pontilhado</span> </p> </td> 
   <td colname="col2"> <p> Configura o estilo de renderização do indicador de definição. </p> <p>Quando definido como <span class="codeph"> dotted </span>, o componente renderiza indicadores idênticos para todas as páginas. </p> <p>Quando definido como <span class="codeph"> numérico</span>, ele coloca um número de página com base em 1 dentro de cada elemento indicador. </p> <p>Não há suporte para o modo de operação <span class="codeph"> numérico</span> em dispositivos com entrada por toque. Em vez disso, o componente usa <span class="codeph"> pontilhado</span> nesses dispositivos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`dotted`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
