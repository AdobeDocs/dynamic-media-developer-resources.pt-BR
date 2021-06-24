---
description: Exibir marcas de impressora. Especifica como exibir as marcas da impressora.
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 6%

---

# printerMark{#printermark}

Exibir marcas de impressora. Especifica como exibir as marcas da impressora.

` printerMark= *`trim `*, *`marksbleed `*, *`marcações registro `*, *`marcações cor `*, *`barspage `*, *``*, *`informações, estilo `*, *`camada de peso incorporar`*`

As diferentes marcas podem ser desativadas ou ativadas. O estilo das marcas de impressora também pode ser controlado.

Estes são os valores válidos:

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>aparar marcas= </p></td> 
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
  <td class="stentry"> <p>barras coloridas= </p></td> 
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
  <td class="stentry"> <p>peso da linha= </p></td> 
  <td class="stentry"> <p>Qualquer valor no intervalo de 0.125 - 2.0, incluindo ambos os valores. </p></td> 
  <td class="stentry"> <p>O padrão é 0,25. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>incorporação de camada= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>O padrão é 1. </p></td> 
 </tr> 
</table>

## Exemplo {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
