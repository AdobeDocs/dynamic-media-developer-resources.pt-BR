---
description: O visualizador exibe regiões de resultados de pesquisa sobre a exibição principal para destacar palavras ou frases encontradas no catálogo.
solution: Experience Manager
title: Efeito de pesquisa
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# Efeito de pesquisa{#search-effect}

O visualizador exibe regiões de resultados de pesquisa sobre a exibição principal para destacar palavras ou frases encontradas no catálogo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

A aparência das regiões de resultados de pesquisa é controlada com o seguinte seletor de classe CSS:

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
   <td colname="col2"> <p>Plano de fundo da região do resultado da pesquisa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar regiões de resultados de pesquisa com um preenchimento amarelo semitransparente:

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```

