---
description: Os arquivos de atributos de catálogo reconhecem esses atributos de solicitação.
seo-description: Os arquivos de atributos de catálogo reconhecem esses atributos de solicitação.
seo-title: Atributos de solicitação
solution: Experience Manager
title: Atributos de solicitação
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 02156b81-9f18-461e-94c1-43b1155c4ab6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---


# Atributos de solicitação{#request-attributes}

Os arquivos de atributos de catálogo reconhecem esses atributos de solicitação.

Sintaxe

<table id="simpletable_2690384A0117458DB12E4E99EFDA975A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> MaxPix</a> </span> </p></td> 
  <td class="stentry"> <p>Limite de tamanho de imagem de resposta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-allowdirecturls.md#reference-cc649a518182497baacf9f6b19559689" type="reference" format="dita" scope="local"> AllowDirectUrls</a> </span> </p></td> 
  <td class="stentry"> <p>Permitir URLs absolutos como fontes de imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> RootUrl</a> </span> </p></td> 
  <td class="stentry"> <p>URL raiz para URLs de origem de imagem relativos. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local"> RequestObfuscation</a> </span> </p></td> 
  <td class="stentry"> <p>Modo de ofuscação de solicitação. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"> RequestLock</a> </span> </p></td> 
  <td class="stentry"> <p>Solicite o modo de bloqueio. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local"> Marca d'água</a> </span> </p></td> 
  <td class="stentry"> <p>Seletor de modelo de marca d'água. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"> ErrorImage</a> </span> </p></td> 
  <td class="stentry"> <p>Imagem de erro ou modelo. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561" type="reference" format="dita" scope="local"> ErrorDetail</a></span> </p></td> 
  <td class="stentry"> <p>Detalhes da mensagem de erro. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-trusteddomains.md#reference-563bd5c54f914d9abcd2304ab292e12f" type="reference" format="dita" scope="local"> TrustedDomains</a> </span> </p></td> 
  <td class="stentry"> <p>Domínios da Web autorizados a acessar imagens de resposta swf. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf" type="reference" format="dita" scope="local"> DefaultExpiration</a> </span> </p></td> 
  <td class="stentry"> <p>TTL do cache do cliente para respostas de imagem padrão. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d" type="reference" format="dita" scope="local"> NonImgExpiration</a> </span> </p></td> 
  <td class="stentry"> <p>TTL do cache do cliente para respostas que não sejam de imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318" type="reference" format="dita" scope="local"> LocaleMap</a></span> </p></td> 
  <td class="stentry"> <p>Mapa de tradução de ID. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e" type="reference" format="dita" scope="local"> LocaleStrMap</a> </span> </p></td> 
  <td class="stentry"> <p>Mapa de localização de cadeia. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local"> DefaultImageMode</a> </span> </p></td> 
  <td class="stentry"> <p>Comportamento padrão da imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68" type="reference" format="dita" scope="local"> ClientAddressFilter</a></span> </p></td> 
  <td class="stentry"> <p>Filtro de endereço IP do cliente. </p></td> 
 </tr> 
</table>

