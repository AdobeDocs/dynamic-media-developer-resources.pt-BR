---
title: DefinirIndicador.modo
description: DefinirIndicador.modo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
TQID: 'https://experienceleague.adobe.com/lss5EqVS8ggpyoDlnGlcagfln977-Hw4fcchN5LMGt4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 65
ht-degree: 0%

---

# DefinirIndicador.modo{#setindicator-mode}

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
