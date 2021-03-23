---
description: Controle de cache. Permite desativar seletivamente o armazenamento em cache no lado do cliente (navegador, servidores proxy, sistemas de armazenamento em cache de rede) e o armazenamento em cache no cache interno do Servidor de Plataforma.
seo-description: Controle de cache. Permite desativar seletivamente o armazenamento em cache no lado do cliente (navegador, servidores proxy, sistemas de armazenamento em cache de rede) e o armazenamento em cache no cache interno do Servidor de Plataforma.
seo-title: cache
solution: Experience Manager
title: cache
uuid: 8af89b67-39d5-43e5-a58d-2cd509a1e373
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---


# cache{#cache}

Controle de cache. Permite desativar seletivamente o armazenamento em cache no lado do cliente (navegador, servidores proxy, sistemas de armazenamento em cache de rede) e o armazenamento em cache no cache interno do Servidor de Plataforma.

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

A palavra-chave &#39; `validate`&#39; permite a atualização das entradas de cache do servidor após a alteração dos arquivos de textura ou vinheta, sem precisar aguardar a expiração automática da entrada de cache. O armazenamento em cache do cliente não é afetado por este comando.

Se especificado em uma solicitação aninhada, `cache=on` habilita o armazenamento em cache persistente no lado do servidor da imagem gerada pela solicitação aninhada. Deve-se tomar cuidado para permitir o armazenamento em cache de solicitações aninhadas somente quando se espera que a mesma solicitação aninhada seja chamada repetidamente com exatamente os mesmos parâmetros.

## Propriedades {#section-0dcbd62e1122400e8c347f408f2d937e}

Pode ocorrer em qualquer lugar na solicitação. Ignorado quando a solicitação não retorna uma imagem de resposta. *`clientControl`* é ignorado quando o armazenamento em cache do lado do cliente é desativado pelo catálogo de materiais (se  `attribute::Expiration` tiver um valor negativo). *`serverControl`* é ignorado se o armazenamento em cache do servidor estiver desativado (  `PlatformServer::cache.enable`).

## Padrão {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` para solicitações HTTP,  `cache=off` para solicitações aninhadas/incorporadas.

## Consulte também {#section-2f5853751dab49579e97418fa766bdf9}

[catálogo::Expiração](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
