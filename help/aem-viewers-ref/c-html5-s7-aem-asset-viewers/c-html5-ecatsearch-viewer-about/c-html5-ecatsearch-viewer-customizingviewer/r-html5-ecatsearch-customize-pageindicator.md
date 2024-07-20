---
title: Indicador de página
description: O indicador da página exibe o índice da página atual e a contagem total de páginas. Ele aparece na barra de controle principal em sistemas desktop e tablet, em telefones celulares é adicionado à barra de controle secundária. O indicador de página pode ser dimensionado, aparado e posicionado por CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 38241e96-ee7f-4dc1-a2a6-4a76e25b00dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# Indicador de página{#page-indicator}

O indicador da página exibe o índice da página atual e a contagem total de páginas. Ele aparece na barra de controle principal em sistemas desktop e tablet, em telefones celulares é adicionado à barra de controle secundária. O indicador de página pode ser dimensionado, aparado e posicionado por CSS.

O indicador da página de aparência é controlado com o seguinte seletor de classe CSS:

`.s7ecatalogsearchviewer .s7pageindicator`

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
   <td colname="col2"> <p>Posição a partir da borda superior da barra de controle principal (em sistemas desktop e tablets) ou da barra de controle secundária (em celulares), incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> direita </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda direita da barra de controle principal (em sistemas desktop e tablets) ou da barra de controle secundária (em celulares), incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> saiu de </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda esquerda da barra de controle principal (em sistemas desktop e tablets) ou da barra de controle secundária (em celulares), incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> inferior </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda inferior da barra de controle principal (em sistemas desktop e tablets) ou da barra de controle secundária (em celulares), incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do indicador de página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do indicador de página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um indicador de página com 56 x 28 pixels, centralizado horizontalmente e posicionado a 4 pixels da parte inferior da barra de controle principal, e usar uma fonte Helvetica® de 14 pixels.

```
.s7ecatalogsearchviewer  .s7pageindicator { 
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
