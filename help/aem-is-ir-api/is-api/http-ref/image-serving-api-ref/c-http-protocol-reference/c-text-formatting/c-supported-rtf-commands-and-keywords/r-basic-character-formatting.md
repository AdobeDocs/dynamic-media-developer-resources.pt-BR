---
description: Use os seguintes comandos para a formatação básica de caracteres.
seo-description: Use os seguintes comandos para a formatação básica de caracteres.
seo-title: Formatação básica de caracteres
solution: Experience Manager
title: Formatação básica de caracteres
topic: Dynamic Media Image Serving - Image Rendering API
uuid: cc8f276a-ebcc-479b-bd86-7ac0dc755f11
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '137'
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
   <td> <span class="codeph"> \plain  </span> </td> 
   <td> <p>Redefina a formatação de caracteres como padrão. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> apenas. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \f  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Face da fonte. </p> </td> 
   <td> <p> <span class="codeph"> \fonttbl  </span> index. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fs  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Tamanho da fonte. </p> </td> 
   <td> <p>Metade dos pontos; o padrão é 24. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cf  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Cor da fonte. </p> </td> 
   <td> <p>Índice baseado em 0 na tabela de cores. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \b  </span> </td> 
   <td> <p>Estilo negrito. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \i  </span> </td> 
   <td> <p>Estilo itálico. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sub  </span> </td> 
   <td> <p>Subscrito. </p> </td> 
   <td> <p>Reduz o tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \super  </span> </td> 
   <td> <p>Sobrescrito. </p> </td> 
   <td> <p>Reduz o tamanho da fonte. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <span class="codeph"> \ul  </span> </td> 
   <td> <p>Sublinhado. </p> </td> 
   <td> <p>O Serviço de imagem também reconhece os seguintes comandos de sublinhado RTF: </p> <p> 
     <ul id="ul_EF2077DD51F94E2E94D8F1FA661F95DE"> 
      <li id="li_F9382148CCCC4A6AB373DD96D28B71EE"> <span class="codeph"> \uld  </span> </li> 
      <li id="li_141276B2082E4AD0A8C7D3BDDADD6EE2"> <span class="codeph"> \uldash  </span> </li> 
      <li id="li_32CE2C69EEFE462FB21F49FF52A65B0B"> <span class="codeph"> \uldashd  </span> </li> 
      <li id="li_DCF3CD4F884845A5A6B84BDD8DB3A572"> <span class="codeph"> \uldashdd  </span> </li> 
      <li id="li_FDEF96CCE14D41BDB878AADCFF73068F"> <span class="codeph"> \uldb  </span> </li> 
      <li id="li_482CCC6F5D8544CCA69DF2A070097ABD"> <span class="codeph"> \ulth  </span> </li> 
      <li id="li_F11C79A6640B4C0684CA5D9733E49F43"> <span class="codeph"> \ulw  </span> </li> 
      <li id="li_84F94D17372B4C0494A9F8AEC951C556"> <span class="codeph"> \ulwave  </span> </li> 
     </ul> </p> <p>Eles são implementados no momento como um sublinhado padrão <span class="codeph"> \ul </span>. Todos os outros comandos de sublinhado RTF são ignorados. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ulnone  </span> </td> 
   <td> <p>desativar sublinhado </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ul0  </span> </td> 
   <td> <p>desativar sublinhado </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \caps  </span> </td> 
   <td> <p>maiúsculo </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> apenas. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \scaps  </span> </td> 
   <td> <p>minúsculo ("versalete") </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> apenas. </p> </td> 
  </tr> 
 </tbody> 
</table>

