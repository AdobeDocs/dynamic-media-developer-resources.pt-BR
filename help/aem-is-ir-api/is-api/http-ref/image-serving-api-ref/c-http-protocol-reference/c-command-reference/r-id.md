---
description: Versão de imagem/metadados. Ao trabalhar com conteúdo que muda frequentemente, os servidores em redes de cache, como Akamai, caches de navegador e caches de servidor proxy corporativo, podem armazenar respostas de disponibilização de imagem que podem estar desatualizadas por períodos de tempo.
seo-description: Versão de imagem/metadados. Ao trabalhar com conteúdo que muda frequentemente, os servidores em redes de cache, como Akamai, caches de navegador e caches de servidor proxy corporativo, podem armazenar respostas de disponibilização de imagem que podem estar desatualizadas por períodos de tempo.
seo-title: id
solution: Experience Manager
title: id
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3d526326-c8fa-4aef-95a9-93ccacf08f73
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# id{#id}

Versão de imagem/metadados. Ao trabalhar com conteúdo que muda frequentemente, os servidores em redes de cache, como Akamai, caches de navegador e caches de servidor proxy corporativo, podem armazenar respostas de disponibilização de imagem que podem estar desatualizadas por períodos de tempo.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val  </span> </span> </p> </td> 
  <td class="stentry"> <p>Sequência de caracteres da versão. </p> </td> 
 </tr> 
</table>

O Serviço de imagem inclui um mecanismo de controle de versão que pode ajudar a reduzir a chance de uma entrada de cache desatualizada ser usada por um aplicativo. Esse mecanismo envolve usar `req=props` para obter strings de identificador de versão para dados de imagem e metadados (como mapa de imagem ou dados de público alvo de zoom). A string do identificador da versão é adicionada às solicitações do Serviço de imagem que podem ser armazenadas em cache com o comando `id=`.

Quando uma imagem de origem ou metadados são alterados, o valor da ID de versão correspondente também será alterado. A inclusão de um valor atualizado da ID da versão com o comando `id=` garante que as entradas antigas do cache não serão mais acessadas.

A tabela a seguir lista as strings de identificador de versão a serem usadas para cada tipo `req=`:

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> <b> identificador de versão de req=props</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> img </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> mapa </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> máscara </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> públicos alvos </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> tmb </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> userdata </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` os tipos não listados acima têm um TTL curto (  `attribute::NonImgExpiration`) ou as suas respostas não podem ser obtidas em cache; não há vantagem em incluir  `id=` esses pedidos.

## Propriedades {#section-62e973d0d5884abebbb0679f9278ae2c}

Atributo de solicitação. Opcional. Sempre ignorado pelo servidor.

## Padrão {#section-96136720c82842c89505347ec39e6024}

Nenhum.

## Exemplo {#section-a5fb871e0ec8485c91c4fca78895d17f}

Consulte a descrição de [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) para obter exemplos de uso.

## Consulte Também {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3),  [catálogo::Expiração](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a),  [atributo::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
