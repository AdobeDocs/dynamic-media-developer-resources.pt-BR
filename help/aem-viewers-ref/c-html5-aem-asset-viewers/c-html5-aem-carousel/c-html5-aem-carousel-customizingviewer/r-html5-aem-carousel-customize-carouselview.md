---
description: A visualização principal consiste na imagem do banner.
seo-description: A visualização principal consiste na imagem do banner.
seo-title: Visualização do carrossel
solution: Experience Manager
title: Visualização do carrossel
topic: Dynamic Media
uuid: bf2065cc-fef2-4d4e-ab2a-a533fa063a80
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---


# Visualização do carrossel{#carousel-view}

A visualização principal consiste na imagem do banner.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS da área do visualizador principal**

A aparência da área de visualização é controlada com o seguinte seletor de classe CSS:

```
.s7carouselviewer .s7carouselview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo em formato hexadecimal da visualização principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a visualização principal transparente.

```
.s7carouselviewer .s7carouselview { 
 background-color: transparent; 
}
```

