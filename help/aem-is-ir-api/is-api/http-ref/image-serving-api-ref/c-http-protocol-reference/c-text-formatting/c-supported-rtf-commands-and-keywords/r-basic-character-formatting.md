---
description: Use os seguintes comandos para a formatação básica de caracteres.
solution: Experience Manager
title: Formatação básica de caracteres
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d3bd6d4d-d7bd-4c9b-bc9e-7edaaac6378e
TQID: 'https://experienceleague.adobe.com/-QEj-7BWb1yXOLxH25Ay6qBDcMJhI8D6VdHNs0bLgUE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 129
ht-degree: 0%

---

# Formatação básica de caracteres{#basic-character-formatting}

Use os seguintes comandos para a formatação básica de caracteres.

<table id="table_65415B84652F4E7497299AD90AE7C191"> 
 <thead> 
  <tr> 
   <th class="entry"> Comando </th> 
   <th class="entry"> Descrição </th> 
   <th class="entry"> Notas </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \simples </span> </td> 
   <td> <p>Redefinir a formatação de caractere para o padrão. </p> </td> 
   <td> <p> <span class="codeph"> somente textPs= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \f <span class="varname"> N </span> </span> </td> 
   <td> <p>Face da fonte. </p> </td> 
   <td> <p> <span class="codeph"> \fonttbl </span> índice. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fs <span class="varname"> N </span> </span> </td> 
   <td> <p>Tamanho da fonte. </p> </td> 
   <td> <p>Meio pontos; o padrão é 24. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cf <span class="varname"> N </span> </span> </td> 
   <td> <p>Cor da fonte. </p> </td> 
   <td> <p>índice com base em 0 na tabela de cores. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \b </span> </td> 
   <td> <p>Estilo negrito. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \i </span> </td> 
   <td> <p>Estilo em itálico. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sub </span> </td> 
   <td> <p>Subscrito. </p> </td> 
   <td> <p>Reduz o tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \super </span> </td> 
   <td> <p>Sobrescrito. </p> </td> 
   <td> <p>Reduz o tamanho da fonte. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <span class="codeph"> \ul </span> </td> 
   <td> <p>Sublinhado. </p> </td> 
   <td> <p>O Servidor de imagens também reconhece os seguintes comandos RTF underline: </p> <p> 
     <ul id="ul_EF2077DD51F94E2E94D8F1FA661F95DE"> 
      <li id="li_F9382148CCCC4A6AB373DD96D28B71EE"> <span class="codeph"> \uld </span> </li> 
      <li id="li_141276B2082E4AD0A8C7D3BDDADD6EE2"> <span class="codeph"> \uldash </span> </li> 
      <li id="li_32CE2C69EEFE462FB21F49FF52A65B0B"> <span class="codeph"> \uldashd </span> </li> 
      <li id="li_DCF3CD4F884845A5A6B84BDD8DB3A572"> <span class="codeph"> \uldashdd </span> </li> 
      <li id="li_FDEF96CCE14D41BDB878AADCFF73068F"> <span class="codeph"> \uldb </span> </li> 
      <li id="li_482CCC6F5D8544CCA69DF2A070097ABD"> <span class="codeph"> \lth </span> </li> 
      <li id="li_F11C79A6640B4C0684CA5D9733E49F43"> <span class="codeph"> \lu </span> </li> 
      <li id="li_84F94D17372B4C0494A9F8AEC951C556"> <span class="codeph"> \ulwave </span> </li> 
     </ul> </p> <p>Eles são implementados no momento como um sublinhado padrão <span class="codeph"> \ul </span>. Todos os outros comandos RTF sublinhados são ignorados. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ulnenhum </span> </td> 
   <td> <p>desativar sublinhado </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ul0 </span> </td> 
   <td> <p>desativar sublinhado </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \caps </span> </td> 
   <td> <p>maiúsculas </p> </td> 
   <td> <p> <span class="codeph"> somente textPs= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \escapes </span> </td> 
   <td> <p>minúsculas ("versalete") </p> </td> 
   <td> <p> <span class="codeph"> somente textPs= </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>
