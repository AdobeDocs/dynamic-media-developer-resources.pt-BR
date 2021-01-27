---
description: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
topic: Dynamic Media
uuid: e60603a5-06dc-43e3-a380-b4d97fc539f1
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 1%

---


# PageView.maxloadradius{#pageview-maxloadradius}

[!DNL `[PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica o comportamento de pré-carregamento do componente. </p> <p>Quando definido como <span class="codeph"> -1</span>, o componente pré-carrega todos os quadros do catálogo quando em um estado ocioso. </p> <p> Quando definido como <span class="codeph"> 0</span>, o componente carrega apenas o quadro que está visível no momento, o quadro anterior e o quadro seguinte. </p> <p>Defina <span class="codeph"><span class="varname"> preloadnbr</span></span> para definir quantos quadros invisíveis ao redor do quadro exibido no momento são pré-carregados em um estado ocioso. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-4b7952997f9240e581d21bcdb173f9af}

Opcional.

## Padrão {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## Exemplo {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
