---
title: Indicador de página
description: O indicador de página exibe o índice de página atual e a contagem total de páginas. Ele aparece na barra de controle principal em sistemas de desktop e tablet, em celulares é adicionado à barra de controle secundária. O indicador de página pode ser dimensionado, esfolado e posicionado por CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: c63af583-274c-4052-8186-604119a368af
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---

# Indicador de página{#page-indicator}

O indicador de página exibe o índice de página atual e a contagem total de páginas. Ele aparece na barra de controle principal em sistemas de desktop e tablet, em celulares é adicionado à barra de controle secundária. O indicador de página pode ser dimensionado, esfolado e posicionado por CSS.

A aparência do indicador de página é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda superior da barra de controle principal (em sistemas de desktop e tablets) ou na barra de controle secundária (em telefones celulares), incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda direita da barra de controle principal (em sistemas de desktop e tablets) ou da barra de controle secundária (em telefones celulares), incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Posição da borda esquerda da barra de controle principal (em sistemas de desktop e tablets) ou da barra de controle secundária (em telefones celulares), incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda inferior da barra de controle principal (em sistemas de desktop e tablets) ou na barra de controle secundária (em telefones celulares), incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do indicador da página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do indicador da página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Cor da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um indicador de página com 56 x 28 pixels, centrado horizontalmente e posicionado 4 pixels a partir da parte inferior da barra de controle principal, e usar uma fonte Helvetica® de 14 pixels.

```
.s7ecatalogviewer  .s7pageindicator { 
 position:absolute; 
 bottom: 4px; 
 margin-left: -28px;  
 left: 50%; 
 width:56px; 
 height:28px; 
 font-family: Helvetica; 
 font-size:14px; 
}
```
