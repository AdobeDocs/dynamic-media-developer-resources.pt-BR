---
title: Efeito de pesquisa
description: O visualizador exibe as regiões de resultado da pesquisa sobre a exibição principal para destacar palavras ou frases encontradas no catálogo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---

# Efeito de pesquisa{#search-effect}

O visualizador exibe as regiões de resultado da pesquisa sobre a exibição principal para destacar palavras ou frases encontradas no catálogo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área do visualizador principal**

A aparência das regiões de resultado de pesquisa é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> plano de fundo </span> </p> </td> 
   <td colname="col2"> <p>Plano de fundo da região de resultados da pesquisa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar regiões de resultados de pesquisa com um preenchimento amarelo semitransparente:

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```
