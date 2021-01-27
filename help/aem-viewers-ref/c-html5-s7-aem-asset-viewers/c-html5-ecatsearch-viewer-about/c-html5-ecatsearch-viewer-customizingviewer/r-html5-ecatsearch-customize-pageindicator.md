---
description: O indicador de página exibe o índice de página atual e a contagem total de páginas. Ela é exibida na barra de controle principal em sistemas de desktop e tablet, em telefones celulares é adicionada à barra de controle secundária. O indicador de página pode ser dimensionado, esfolado e posicionado pelo CSS.
seo-description: O indicador de página exibe o índice de página atual e a contagem total de páginas. Ela é exibida na barra de controle principal em sistemas de desktop e tablet, em telefones celulares é adicionada à barra de controle secundária. O indicador de página pode ser dimensionado, esfolado e posicionado pelo CSS.
seo-title: Indicador de página
solution: Experience Manager
title: Indicador de página
topic: Dynamic Media
uuid: 1be6021b-3026-48ef-b121-eeb8270d2bae
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# Indicador de página{#page-indicator}

O indicador de página exibe o índice de página atual e a contagem total de páginas. Ela é exibida na barra de controle principal em sistemas de desktop e tablet, em telefones celulares é adicionada à barra de controle secundária. O indicador de página pode ser dimensionado, esfolado e posicionado pelo CSS.

O indicador de página de aparência é controlado com o seguinte seletor de classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda superior da barra de controle principal (em sistemas de desktop e tablets) ou da barra de controle secundária (em telefones celulares), incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posição na borda direita da barra de controle principal (em sistemas de desktop e tablets) ou na barra de controle secundária (em telefones celulares), incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p>Posição da borda esquerda da barra de controle principal (em sistemas de desktop e tablets) ou da barra de controle secundária (em telefones celulares), incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posição na borda inferior da barra de controle principal (em sistemas de desktop e tablets) ou na barra de controle secundária (em telefones celulares), incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do indicador de página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do indicador de página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor  </span> </p> </td> 
   <td colname="col2"> <p>Cor da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um indicador de página de 56 x 28 pixels, horizontalmente centralizado e posicionado 4 pixels a partir da parte inferior da barra de controle principal, e usar uma fonte Helvetica de 14 pixels.

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

