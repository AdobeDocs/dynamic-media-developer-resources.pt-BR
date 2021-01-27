---
description: O visualizador exibe regiões de resultados de pesquisa na visualização principal para realçar palavras ou frases encontradas no catálogo.
seo-description: O visualizador exibe regiões de resultados de pesquisa na visualização principal para realçar palavras ou frases encontradas no catálogo.
seo-title: Efeito de pesquisa
solution: Experience Manager
title: Efeito de pesquisa
topic: Dynamic Media
uuid: 3a076ff8-2da5-4020-8a77-8f5a256afefe
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# Efeito de pesquisa{#search-effect}

O visualizador exibe regiões de resultados de pesquisa na visualização principal para realçar palavras ou frases encontradas no catálogo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS da área do visualizador principal**

A aparência das regiões de resultado da pesquisa é controlada com o seguinte seletor de classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> fundo  </span> </p> </td> 
   <td colname="col2"> <p>Plano de fundo da região de resultados da pesquisa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar regiões de resultado de pesquisa com um preenchimento amarelo semitransparente:

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```

