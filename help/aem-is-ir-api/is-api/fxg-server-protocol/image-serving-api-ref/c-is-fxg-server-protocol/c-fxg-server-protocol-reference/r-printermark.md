---
description: Exibir marcas da impressora. Especifica como exibir as marcas de impressora.
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# printerMark{#printermark}

Exibir marcas da impressora. Especifica como exibir as marcas de impressora.

` printerMark= *`marcas de aparagem`*, *`marcas de sangria`*, *`marcas de registro`*, *`barras de cor`*, *`informações de página`*, *`estilo`*, *`espessura da linha`*, *`camada incorporada`*`

As diferentes marcas podem ser desativadas ou ativadas. O estilo das marcas da impressora também pode ser controlado.

Estes são os valores válidos:

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>marcas de aparagem= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>O padrão é 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>marcas de sangria= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>O padrão é 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>marcas de registro= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>O padrão é 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>barras de cores= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>O padrão é 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>informações da página= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>O padrão é 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>Padrão </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>O padrão é o padrão </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>espessura da linha= </p></td> 
  <td class="stentry"> <p>Qualquer valor no intervalo de 0,125 a 2,0, incluindo ambos os valores. </p></td> 
  <td class="stentry"> <p>O padrão é 0,25. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>camada incorporada= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>O padrão é 1. </p></td> 
 </tr> 
</table>

## Exemplo {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
