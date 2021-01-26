---
description: Controle de cache. Permite desativar seletivamente o cache do lado do cliente (navegador, servidores proxy, sistemas de cache de rede) e o cache no cache interno do Servidor de plataforma.
seo-description: Controle de cache. Permite desativar seletivamente o cache do lado do cliente (navegador, servidores proxy, sistemas de cache de rede) e o cache no cache interno do Servidor de plataforma.
seo-title: cache
solution: Experience Manager
title: cache
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8af89b67-39d5-43e5-a58d-2cd509a1e373
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---


# cache{#cache}

Controle de cache. Permite desativar seletivamente o cache do lado do cliente (navegador, servidores proxy, sistemas de cache de rede) e o cache no cache interno do Servidor de plataforma.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>on | desligado | validar </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl  </span> </p> </td> 
  <td class="stentry"> <p>on | desligado </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl  </span> </p></td> 
  <td class="stentry"> <p>on | desligado </p></td> 
 </tr> 
</table>

Se apenas um valor *`cacheControl`* for especificado, ele será aplicado aos caches do cliente e do servidor.

A palavra-chave &#39; `validate`&#39; permite a atualização das entradas do cache do servidor depois que os arquivos de textura ou vinheta forem alterados, sem precisar aguardar a entrada do cache expirar automaticamente. O cache do cliente não é afetado por este comando.

Se especificado em uma solicitação aninhada, `cache=on` habilita o armazenamento em cache persistente no lado do servidor da imagem gerada pela solicitação aninhada. Deve-se ter cuidado para ativar o armazenamento em cache para solicitações aninhadas somente quando se espera que a mesma solicitação aninhada seja chamada repetidamente com exatamente os mesmos parâmetros.

## Propriedades {#section-0dcbd62e1122400e8c347f408f2d937e}

Pode ocorrer em qualquer lugar na solicitação. Ignorado quando a solicitação não retorna uma imagem de resposta. *`clientControl`* é ignorada quando o cache do lado do cliente é desativado pelo catálogo de materiais (se  `attribute::Expiration` tiver um valor negativo). *`serverControl`* é ignorada se o armazenamento em cache do servidor estiver desativado (  `PlatformServer::cache.enable`).

## Padrão {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` para solicitações HTTP,  `cache=off` para solicitações aninhadas/incorporadas.

## Consulte também {#section-2f5853751dab49579e97418fa766bdf9}

[catálogo::Expiração](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
