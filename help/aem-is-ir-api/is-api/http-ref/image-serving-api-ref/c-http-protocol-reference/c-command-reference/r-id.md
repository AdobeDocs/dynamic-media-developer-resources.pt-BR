---
title: id
description: Versão da imagem/metadados. Ao trabalhar com conteúdo que muda com frequência, os servidores no armazenamento em cache de redes, como Akamai, caches de navegador e caches de servidor proxy corporativo podem armazenar respostas do Servidor de imagens que podem estar desatualizadas por períodos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# id{#id}

Versão da imagem/metadados. Ao trabalhar com conteúdo que muda com frequência, os servidores no armazenamento em cache de redes, como Akamai, caches de navegador e caches de servidor proxy corporativo podem armazenar respostas do Servidor de imagens que podem estar desatualizadas por períodos.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val </span> </span> </p> </td> 
  <td class="stentry"> <p>String de versão. </p> </td> 
 </tr> 
</table>

O Servidor de imagens inclui um mecanismo de controle de versão que pode ajudar a reduzir a chance de uma entrada de cache desatualizada ser usada por um aplicativo. Esse mecanismo envolve o uso de `req=props` para obter cadeias de caracteres do identificador de versão para dados de imagem e metadados (como mapa de imagem ou dados de destino de zoom). A cadeia de caracteres do identificador de versão é adicionada às solicitações do Servidor de imagens armazenáveis em cache com o comando `id=`.

Quando uma imagem de origem ou metadados são alterados, o valor da ID da versão correspondente também é alterado. A inclusão de um valor atualizado de ID de versão com o comando `id=` garante que as entradas de cache antigas não possam mais ser acessadas.

A tabela a seguir lista as cadeias de caracteres do identificador de versão a serem usadas para cada tipo `req=`:

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= tipo</b> </th> 
   <th class="entry"> Identificador de versão <b> de req=props</b> </th> 
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
   <td> <p> targets </p> </td> 
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

`req=` tipos não listados acima têm um TTL curto ( `attribute::NonImgExpiration`) ou suas respostas não são armazenáveis em cache; não há vantagem em incluir `id=` com essas solicitações.

## Propriedades {#section-62e973d0d5884abebbb0679f9278ae2c}

Solicitar atributo. Opcional. Sempre ignorado pelo servidor.

## Padrão {#section-96136720c82842c89505347ec39e6024}

Nenhum.

## Exemplo {#section-a5fb871e0ec8485c91c4fca78895d17f}

Consulte a descrição de [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) para obter um exemplo de uso.

## Consulte Também {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
