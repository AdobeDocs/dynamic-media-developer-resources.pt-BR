---
title: Efeito de pesquisa
description: O visualizador exibe as regiões de resultado da pesquisa sobre a exibição principal para destacar palavras ou frases encontradas no catálogo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
TQID: 'https://experienceleague.adobe.com/h30DfEeB69i1gbnfOvnKphglRkXgcvOTG8L-eTZv2GU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 85
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

