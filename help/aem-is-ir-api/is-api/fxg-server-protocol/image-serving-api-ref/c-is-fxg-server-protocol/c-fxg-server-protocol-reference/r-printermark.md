---
description: Exibir marcas de impressora. Especifica como exibir as marcas da impressora.
seo-description: Exibir marcas de impressora. Especifica como exibir as marcas da impressora.
seo-title: printerMark
solution: Experience Manager
title: printerMark
topic: Scene7 Image Serving - Image Rendering API
uuid: 3e5699ce-3ccd-4f85-91dd-c40c252a758d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# printerMark{#printermark}

Exibir marcas de impressora. Especifica como exibir as marcas da impressora.

` printerMark= *`aparar`*, *`marcas`*, *`marcas de sangria marcas de registro`*, *`marcas`*, *`de cores da barra de`*, *``*, *`informações`*, *`stylelineweight`*`

As diferentes marcas podem ser desativadas ou ativadas. O estilo das marcas de impressora também pode ser controlado.

Estes são os valores válidos:

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>aparm marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>O padrão é 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>sangria= </p></td> 
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
  <td class="stentry"> <p>O padrão é Padrão </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>peso de linha= </p></td> 
  <td class="stentry"> <p>Qualquer valor no intervalo 0.125 - 2.0, incluindo ambos os valores. </p></td> 
  <td class="stentry"> <p>O padrão é 0,25. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>camada incorporada= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>O padrão é 1. </p></td> 
 </tr> 
</table>

## Example {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
