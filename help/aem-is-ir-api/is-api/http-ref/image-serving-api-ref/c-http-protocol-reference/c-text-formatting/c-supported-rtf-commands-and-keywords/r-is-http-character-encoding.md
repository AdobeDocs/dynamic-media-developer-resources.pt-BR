---
title: Codificação de caracteres
description: Use os seguintes comandos para codificar caracteres.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# Codificação de caracteres{#character-encoding}

Use os seguintes comandos para codificar caracteres.

<table id="table_EB0C1B674BEA4A37964FB4BF559E0005"> 
 <thead> 
  <tr> 
   <th class="entry"> Comando </th> 
   <th class="entry"> Descrição </th> 
   <th class="entry"> Notas </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph">\'<span class="varname"> HH</span></span> </td> 
   <td> <p>Caractere único de 8 bits. </p> </td> 
   <td> <p><span class="varname"> HH</span> deve ser um valor hexadecimal de 2 dígitos. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>Caractere Unicode único. </p> </td> 
   <td> <p><span class="varname"> N</span> é um inteiro de 2 bytes assinado e, portanto, um valor Unicode maior que 32767 deve ser expresso como um número negativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Tamanho de caractere Unicode. </p> </td> 
   <td> <p>Número de bytes correspondentes a um determinado caractere Unicode. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>Caracteres da área ANSI inferior. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qual </span> </td> 
   <td> <p>Caracteres da área ANSI superior. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>Caracteres de byte duplo seguem. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
