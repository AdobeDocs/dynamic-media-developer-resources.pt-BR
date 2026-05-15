---
title: cache
description: Controle de cache. Permite desabilitar seletivamente o cache do lado do cliente (navegador, servidores proxy, sistemas de cache de rede) e o cache no cache interno  [!DNL Platform Server] .
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
TQID: 'https://experienceleague.adobe.com/xq-8hE9RB7I-CMb-yguhBcEttxTv6IRRHWzh0lDvn6E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 0%

---

# cache {#cache}

Controle de cache. Permite desabilitar seletivamente o cache do lado do cliente (navegador, servidores proxy, sistemas de cache de rede) e o cache no cache interno [!DNL Platform Server].

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>em | desativado | validar </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>em | desativado </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>em | desativado </p></td> 
 </tr> 
</table>

Se apenas um valor *`cacheControl`* for especificado, ele será aplicado aos caches do cliente e do servidor.

A palavra-chave &#39; `validate`&#39; permite atualizar entradas de cache do servidor após arquivos de textura ou vinheta serem alterados, sem precisar aguardar a expiração automática da entrada de cache. O cache do cliente não é afetado por esse comando.

Se especificado em uma solicitação aninhada, `cache=on` habilita o cache persistente do lado do servidor da imagem gerada pela solicitação aninhada. Certifique-se de ativar o armazenamento em cache para solicitações aninhadas somente quando a mesma solicitação aninhada for chamada repetidamente com os mesmos parâmetros.

## Propriedades {#section-0dcbd62e1122400e8c347f408f2d937e}

Pode ocorrer em qualquer lugar na solicitação. Ignorado quando a solicitação não retorna uma imagem de resposta. A propriedade *`clientControl`* é ignorada quando o cache do lado do cliente é desabilitado pelo catálogo de materiais (se `attribute::Expiration` tiver um valor negativo). A propriedade *`serverControl`* será ignorada se o cache do servidor estiver desabilitado ( `PlatformServer::cache.enable`).

## Padrão {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` Para solicitações HTTP, `cache=off` para solicitações aninhadas/inseridas.

## Consulte também {#section-2f5853751dab49579e97418fa766bdf9}

[catálogo::Expiração](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
