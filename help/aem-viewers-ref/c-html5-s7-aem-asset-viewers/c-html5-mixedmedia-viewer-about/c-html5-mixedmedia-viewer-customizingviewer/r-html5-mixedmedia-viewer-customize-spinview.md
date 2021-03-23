---
description: A exibição principal consiste na imagem de rotação quando o ativo atual é um conjunto de rotação.
seo-description: A exibição principal consiste na imagem de rotação quando o ativo atual é um conjunto de rotação.
seo-title: Exibição em rotação
solution: Experience Manager
title: Exibição em rotação
uuid: f1edbcc4-966a-4ec6-8ba9-a76f3ae51733
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# Exibição de rotação{#spin-view}

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

