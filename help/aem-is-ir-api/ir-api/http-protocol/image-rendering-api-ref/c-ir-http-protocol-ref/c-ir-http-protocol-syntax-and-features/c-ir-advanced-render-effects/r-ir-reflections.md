---
title: Reflexões
description: Vinhetas podem ser criadas para incluir dados de reflexão quase 3D.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# Reflexões{#reflections}

Vinhetas podem ser criadas para incluir dados de reflexão quase 3D.

Se tal for criado, são utilizados os seguintes atributos de material para definir as propriedades da superfície refletora do material:

<table id="table_8769C726A17E412FB41F7CB87690B1FE"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Atributo </p> </th> 
   <th class="entry"> <p>Descrição </p> </th> 
   <th class="entry"> <p>Padrão </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> brilho=</span> </a> </p> </td> 
   <td> <p>Brilho da superfície </p> </td> 
   <td> <p>Da vinheta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap= </span> </a> </p> </td> 
   <td> <p>Variação de brilho (imagem em escala de cinza) </p> </td> 
   <td> <p>Nenhum </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> bruxo= </span> </a> </p> </td> 
   <td> <p>Rugosidade da superfície </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>Tipo de material </p> </td> 
   <td> <p>0 (desconhecido) </p> </td> 
  </tr> 
 </tbody> 
</table>

O renderizador ajusta o intervalo da variável `gloss=` e `rough=` de acordo com `type=`. Alguns tipos de materiais, como o tecido, são menos reflexivos do que os tipos de materiais, como pedra ou metal. Além disso, a mesma quantidade de brilho especificada para um resulta frequentemente num efeito de reflexão diferente do outro. O atributo `gloss=` e rugosidade têm uma gama bastante ampla se `type=` não foi especificado ou está definido como `0`.

`glossmap=` Usado para controlar a luminosidade de um material com base em pixel.
