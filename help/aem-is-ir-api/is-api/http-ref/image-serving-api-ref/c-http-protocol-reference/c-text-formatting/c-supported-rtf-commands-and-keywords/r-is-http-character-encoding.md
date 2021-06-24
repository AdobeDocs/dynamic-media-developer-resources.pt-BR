---
description: Use os seguintes comandos para codificação de caracteres.
solution: Experience Manager
title: Codificação de caracteres
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Codificação de caracteres{#character-encoding}

Use os seguintes comandos para codificação de caracteres.

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
   <td> <p>Um caractere de 8 bits. </p> </td> 
   <td> <p><span class="varname"> </span> Ele deve ser um valor hexadecimal de 2 dígitos. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> uN</span></span> </td> 
   <td> <p>Caractere Unicode único. </p> </td> 
   <td> <p><span class="varname"> </span> Nis a signed 2 byte integer e, portanto, um valor Unicode maior que 32767 deve ser expresso como um número negativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> ucN</span></span> </td> 
   <td> <p>Tamanho de caractere Unicode. </p> </td> 
   <td> <p>Número de bytes correspondentes a determinado caractere Unicode. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch  </span> </td> 
   <td> <p>Seguem-se os caracteres de área baixa de ANSI. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \que  </span> </td> 
   <td> <p>Seguem-se os caracteres da área alta de ANSI. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch  </span> </td> 
   <td> <p>Seguem-se os caracteres de byte duplo. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
