---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
topic: Dynamic Media
uuid: 11458300-4a1b-4623-8ea1-db804daab3cf
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---


# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> passo</span></span> </p> </td> 
   <td colname="col2"> <p> Configura o número de ações de aumentar e diminuir o zoom necessárias para aumentar ou diminuir a resolução em um fator de dois. A alteração de resolução para cada ação de zoom é de 2^1 por etapa. Defina como <span class="codeph"> 0</span> para aplicar zoom em resolução total com uma única ação de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> limite</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica a resolução máxima de zoom, relativa à imagem de resolução total. O padrão é <span class="codeph"> 1.0</span>, o que não permite o zoom além da resolução total. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-636d35a4791447039f1902973f568320}

Opcional.

## Padrão {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## Exemplo {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
