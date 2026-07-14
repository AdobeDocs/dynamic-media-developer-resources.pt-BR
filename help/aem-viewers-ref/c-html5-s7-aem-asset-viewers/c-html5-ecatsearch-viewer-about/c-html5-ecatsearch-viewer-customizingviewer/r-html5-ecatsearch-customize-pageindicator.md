---
title: Indicador de página
description: O indicador da página exibe o índice da página atual e a contagem total de páginas. Ele aparece na barra de controle principal em sistemas desktop e tablet, em telefones celulares é adicionado à barra de controle secundária. O indicador de página pode ser dimensionado, aparado e posicionado por CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 38241e96-ee7f-4dc1-a2a6-4a76e25b00dc
TQID: 'https://experienceleague.adobe.com/QikQn00CFMxmnTEXKZcTifhXC-SBmW-IC9VbKlZ7TGY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 258
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
