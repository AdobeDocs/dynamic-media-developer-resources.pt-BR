---
description: Os campos a seguir são reconhecidos em arquivos de dados de imagem e SVG.
solution: Experience Manager
title: Dados Image_SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5392e08f-3614-4588-8846-4262d32f3ce1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# Dados Image_SVG{#image-svg-data}

Os campos a seguir são reconhecidos em arquivos de dados de imagem e SVG.

## Gerenciamento de catálogo {#section-1056bcc3b6d04166b3aa6ec48913b6b2}

<table id="table_823F89CAD494441690D28F18005F774C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md" type="reference" format="dita" scope="local"> Id</a></span> </p> </td> 
   <td colname="col2"> <p>Identificador de registro de catálogo (chave de índice). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Atributos da solicitação {#section-cfe69bcdcd4b4d129e99d11b9078ae4a}

<table id="table_C070C676835F49918E1B3BBF81471B09"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba" type="reference" format="dita" scope="local"> DigimarcInfo</a></span> </p> </td> 
   <td colname="col2"> <p>Informações específicas da imagem para incorporação do Digimarc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a" type="reference" format="dita" scope="local"> Expiração</a></span> </p> </td> 
   <td colname="col2"> <p>Expiração do cache (tempo de vida útil) para imagens de resposta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md" type="reference" format="dita" scope="local"> Modificador</a> </span> </p> </td> 
   <td colname="col2"> <p>Prefixar modificadores de solicitação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md" type="reference" format="dita" scope="local"> PostModifier</a> </span> </p> </td> 
   <td colname="col2"> <p>Modificadores de solicitação Postfix. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded" type="reference" format="dita" scope="local"> Carimbo de data/hora</a></span> </p> </td> 
   <td colname="col2"> <p>Carimbo de data/hora de modificação de arquivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Atributos da imagem {#section-74c4d124255d4218ade87d7d1677c76d}

<table id="table_F2A33C2EB17A4EACB00DDEF7FB1BB0D4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md" type="reference" format="dita" scope="local"> Âncora</a></span> </p> </td> 
   <td colname="col2"> <p>Ponto de ancoragem da imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md" type="reference" format="dita" scope="local"> MaskPath</a></span> </p> </td> 
   <td colname="col2"> <p>Caminho do arquivo de máscara. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md" type="reference" format="dita" scope="local"> Caminho</a></span> </p> </td> 
   <td colname="col2"> <p>Caminho do arquivo de imagem/SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5" type="reference" format="dita" scope="local"> ResoluçãoImpressão</a></span> </p> </td> 
   <td colname="col2"> <p>Resolução de impressão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1" type="reference" format="dita" scope="local"> Resolução</a></span> </p> </td> 
   <td colname="col2"> <p>Resolução do objeto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-size-cat.md" type="reference" format="dita" scope="local"> Tamanho</a></span> </p> </td> 
   <td colname="col2"> <p>Tamanho da imagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Atributos de miniatura {#section-c5ac27bcd4224a80b7f42ead249027b1}

<table id="table_E07909B6C16F4D9686ADA381A4178E25"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69" type="reference" format="dita" scope="local"> ThumbRes</a></span> </p> </td> 
   <td colname="col2"> <p>Resolução da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03" type="reference" format="dita" scope="local"> ThumbType</a></span> </p> </td> 
   <td colname="col2"> <p>Tipo de miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Dados auxiliares {#section-bff4e1f9af9d45f1872abac3b414a629}

<table id="table_B6A9A702F533494E85CEC1AD42EC728A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-assettype-cat.md" type="reference" format="dita" scope="local"> AssetType</a></span> </p> </td> 
   <td colname="col2"> <p>Tipo de ativo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md" type="reference" format="dita" scope="local"> ImageSet</a></span> </p> </td> 
   <td colname="col2"> <p>Dados do conjunto de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md" type="reference" format="dita" scope="local"> Mapa</a></span> </p> </td> 
   <td colname="col2"> <p>Dados do mapa de imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md" type="reference" format="dita" scope="local"> Destinos</a></span> </p> </td> 
   <td colname="col2"> <p>Dados de destino do zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md" type="reference" format="dita" scope="local"> Dados do Usuário</a></span> </p> </td> 
   <td colname="col2"> <p>Dados definidos pelo usuário. </p> </td> 
  </tr> 
 </tbody> 
</table>
