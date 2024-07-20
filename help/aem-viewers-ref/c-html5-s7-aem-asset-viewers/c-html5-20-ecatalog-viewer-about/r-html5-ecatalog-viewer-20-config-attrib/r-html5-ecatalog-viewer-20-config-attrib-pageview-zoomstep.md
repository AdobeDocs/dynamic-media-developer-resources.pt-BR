---
title: PageView.zoomstep
description: PageView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 64cce312-c13b-49c7-af85-3349ff5c4322
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *`etapa`*[, *`limite`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> etapa</span></span> </p> </td> 
   <td colname="col2"> <p> Configura o número de ações de aumento e diminuição de zoom necessárias para aumentar ou diminuir a resolução por um fator de dois. A alteração da resolução para cada ação de zoom é de 2^1 por etapa. Defina como <span class="codeph"> 0</span> para aumentar a resolução total com uma única ação de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> limite</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica a resolução máxima de zoom, relativa à resolução de imagem máxima. O padrão é <span class="codeph"> 1.0</span>, o que não permite aplicar zoom além da resolução máxima. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-636d35a4791447039f1902973f568320}

Opcional.

## Padrão {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## Exemplo {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
