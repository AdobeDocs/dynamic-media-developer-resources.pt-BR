---
description: A exibição principal consiste na imagem estática.
solution: Experience Manager
title: Exibição de zoom
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner
exl-id: e83d53a1-bee9-4e4d-8295-a3a350f3ff9c
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# Visualização de zoom{#zoom-view}

A exibição principal consiste na imagem estática.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

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
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo em formato hexadecimal da exibição principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a exibição principal transparente.

```
.s7interactiveimage .s7zoomview { 
 background-color: transparent; 
}
```
