---
description: Use os seguintes comandos para codificação de caracteres.
seo-description: Use os seguintes comandos para codificação de caracteres.
seo-title: Codificação de caracteres
solution: Experience Manager
title: Codificação de caracteres
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b19b831-b40c-4f26-83a4-732c578dbbf0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '95'
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
   <td> <p>Um caractere único de 8 bits. </p> </td> 
   <td> <p><span class="varname"> HH</span> deve ser um valor hexadecimal de 2 dígitos. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> uN</span></span> </td> 
   <td> <p>Caractere Unicode único. </p> </td> 
   <td> <p><span class="varname"> </span> Nis é um número inteiro de 2 bytes assinado e, portanto, um valor Unicode maior que 32767 deve ser expresso como um número negativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> ucN</span></span> </td> 
   <td> <p>Tamanho de caractere Unicode. </p> </td> 
   <td> <p>Número de bytes correspondentes a determinado caractere Unicode. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch  </span> </td> 
   <td> <p>Seguem-se os caracteres de área ANSI baixa. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich  </span> </td> 
   <td> <p>Seguem-se os caracteres da área ANSI alta. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch  </span> </td> 
   <td> <p>Caracteres de duplo byte seguem. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

