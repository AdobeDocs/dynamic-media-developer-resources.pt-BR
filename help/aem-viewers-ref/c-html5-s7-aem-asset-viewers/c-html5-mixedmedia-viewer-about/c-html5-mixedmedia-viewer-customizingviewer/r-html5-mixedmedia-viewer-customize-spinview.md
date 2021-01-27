---
description: A visualização principal consiste na imagem de rotação quando o ativo atual é um conjunto de rotação.
seo-description: A visualização principal consiste na imagem de rotação quando o ativo atual é um conjunto de rotação.
seo-title: Visualização de rotação
solution: Experience Manager
title: Visualização de rotação
topic: Dynamic Media
uuid: f1edbcc4-966a-4ec6-8ba9-a76f3ae51733
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# Visualização de rotação{#spin-view}

A visualização principal consiste na imagem de rotação quando o ativo atual é um conjunto de rotação.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS da área do visualizador principal**

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
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo no formato hexadecimal da visualização de rotação. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a visualização de rotação transparente.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```

