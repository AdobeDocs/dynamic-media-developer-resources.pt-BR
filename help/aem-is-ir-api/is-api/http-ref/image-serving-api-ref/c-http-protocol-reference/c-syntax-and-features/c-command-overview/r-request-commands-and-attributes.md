---
title: Comandos de solicitação
description: Esses comandos se aplicam independentemente de onde aparecem na solicitação.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3f794f46-e7f0-4899-90fa-898a698dd629
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Comandos de solicitação{#request-commands}

Esses comandos se aplicam independentemente de onde aparecem na solicitação.

<table id="simpletable_3F7C17FB9E374EFDAD01EB24F57EC367"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> cache</a> </p></td> 
  <td class="stentry"> <p>Substitui o comportamento padrão do cache de resposta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2" type="reference" format="dita" scope="local"> imagemPadrão</a> </p></td> 
  <td class="stentry"> <p>Especifica a imagem a ser usada em vez de um arquivo de imagem ausente. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt</a> </p></td> 
  <td class="stentry"> <p>Especifica o formato da imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517" type="reference" format="dita" scope="local"> icc</a> </p></td> 
  <td class="stentry"> <p>Define o perfil de cor de saída. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local">iccEmbed</a> </p> </td> 
  <td class="stentry"> <p>Incorpora o perfil de cores na imagem de resposta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed</a> </p></td> 
  <td class="stentry"> <p>Incorpora os dados de caminho do Photoshop na imagem de resposta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed</a> </p></td> 
  <td class="stentry"> <p>Incorpora metadados de XMP na imagem de resposta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-printres.md#reference-84f52afff4704c4b9d58e4bbbaea1491" type="reference" format="dita" scope="local"> printRes</a> </p> </td> 
  <td class="stentry"> <p>Especifica o valor de resolução de impressão incorporado na imagem de resposta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt</a> </p></td> 
  <td class="stentry"> <p>Especifica os atributos de codificação de JPEG. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38" type="reference" format="dita" scope="local"> quantizar</a> </p> </td> 
  <td class="stentry"> <p>Especifica atributos de quantização de cores para saída de GIF. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req</a> </p></td> 
  <td class="stentry"> <p>Seleciona o tipo de solicitação. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md#reference-29a398cc59dc4caf9acd5f69c9ba9715" type="reference" format="dita" scope="local">resMode</a> </p></td> 
  <td class="stentry"> <p>Especifica o modo de reamostragem ou interpolação da imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14" type="reference" format="dita" scope="local"> modelo</a> </p> </td> 
  <td class="stentry"> <p>Especifica um modelo de composição. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb" type="reference" format="dita" scope="local"> localidade</a> </p></td> 
  <td class="stentry"> <p>Especifica um modelo de composição. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id</a> </p> </td> 
  <td class="stentry"> <p>ID da versão de imagem/metadados. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3" type="reference" format="dita" scope="local"> imageSet</a> </p> </td> 
  <td class="stentry"> <p>Especifica o conjunto de imagens a ser usado para esta solicitação. </p></td> 
 </tr> 
</table>
