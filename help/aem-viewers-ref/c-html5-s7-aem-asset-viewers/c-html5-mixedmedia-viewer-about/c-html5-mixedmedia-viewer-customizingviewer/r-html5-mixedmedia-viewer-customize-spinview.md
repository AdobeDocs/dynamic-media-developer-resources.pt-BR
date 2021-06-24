---
description: A exibição principal consiste na imagem de rotação quando o ativo atual é um conjunto de rotação.
solution: Experience Manager
title: Exibição em rotação
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Developer,Business Practitioner
exl-id: aafc1299-b09a-4379-bd8f-b564066175bd
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---

# Exibição em rotação{#spin-view}

A exibição principal consiste na imagem de rotação quando o ativo atual é um conjunto de rotação.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

A aparência da área de visualização é controlada com o seguinte seletor de classe CSS:

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col2"> <p> Cor do plano de fundo no formato hexadecimal da exibição de rotação. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a exibição de rotação transparente.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```
