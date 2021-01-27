---
description: A visualização principal consiste na imagem estática.
seo-description: A visualização principal consiste na imagem estática.
seo-title: Visualização de zoom
solution: Experience Manager
title: Visualização de zoom
topic: Dynamic Media
uuid: d8349f8c-134f-4e74-9d0c-ab56981965d7
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---


# Visualização de zoom{#zoom-view}

A visualização principal consiste na imagem estática.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS da área do visualizador principal**

A aparência da área de visualização é controlada com o seguinte seletor de classe CSS:

```
.s7interactiveimage .s7zoomview
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
.s7interactiveimage .s7zoomview { 
 background-color: transparent; 
}
```

