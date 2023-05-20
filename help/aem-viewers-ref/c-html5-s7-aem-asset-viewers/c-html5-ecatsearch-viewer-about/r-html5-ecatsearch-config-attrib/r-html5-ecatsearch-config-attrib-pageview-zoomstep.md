---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d92e56ae-2bb6-46f6-b0f7-64b867492a37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# PageView.zoomstep{#pageview-zoomstep}

[!DNL `[PageView.|<containerId>_pageView.]zoomstep= *`etapa`*[, *`limite`*]`]

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> etapa</span></span> </p> </td> 
   <td colname="col2"> <p> Configura o número de ações de aumento e diminuição de zoom necessárias para aumentar ou diminuir a resolução por um fator de dois. A alteração da resolução para cada ação de zoom é de 2^1 por etapa. Defina como <span class="codeph"> 0</span> para aumentar a resolução total com uma única ação de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> limite</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica a resolução máxima de zoom, relativa à resolução de imagem máxima. O padrão é <span class="codeph"> 1.0</span>, que não permite aplicar zoom além da resolução máxima. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-636d35a4791447039f1902973f568320}

Opcional.

## Padrão {#section-ad8a5fe2383e4c228bf177a41b53d921}

[!DNL `1,1`]

## Exemplo {#section-1e20672d42c845bd84f02f88cbc53efc}

[!DNL `zoomstep=2,3`]
