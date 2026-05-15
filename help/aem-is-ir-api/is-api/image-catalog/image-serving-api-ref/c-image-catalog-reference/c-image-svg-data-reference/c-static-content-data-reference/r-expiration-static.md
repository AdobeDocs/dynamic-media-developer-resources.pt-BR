---
title: Expiração
description: Usado para gerenciar o cache do cliente e do servidor proxy. O servidor calcula a hora/data de expiração dos dados de resposta HTTP adicionando esse valor à hora/data de transmissão.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 064dab12-5f58-4e19-a6b1-fbd20182e3aa
TQID: 'https://experienceleague.adobe.com/18Zmoy7bkC58X6KaK2T1FGVTOPrNrLgdQxwbw8jgMT0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 306
ht-degree: 0%

---

# Expiração{#expiration}

Usado para gerenciar o cache do cliente e do servidor proxy. O servidor calcula a hora/data de expiração dos dados de resposta HTTP adicionando esse valor à hora/data de transmissão.

Os navegadores gerenciam caches usando tempos de expiração de arquivos. Antes de passar uma solicitação para o servidor, o navegador verifica seu cache para ver se o arquivo já foi baixado. Em caso positivo, e se o arquivo ainda não tiver expirado, o navegador enviará uma solicitação GET condicional (por exemplo, com o campo If-Modified-Since definido no cabeçalho da solicitação) em vez de uma solicitação GET normal. O servidor tem a opção de responder com um status &quot;304&quot; e não transmitir a imagem. O navegador carrega o arquivo do cache. Isso pode aumentar substancialmente o desempenho geral dos dados acessados com frequência.

A expiração é usada para estes tipos de resposta:

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

Determinados tipos de respostas (por exemplo, respostas de erro) são sempre marcados para expiração imediata (ou marcados como não armazenáveis em cache), enquanto outros (por exemplo, respostas de propriedade ou de imagem padrão) usam configurações de expiração especiais ( `attribute::NonImgExpiration` e `attribute::DefaultExpiration`).

## Propriedades {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

Número real, -2, -1, ou 0 ou maior. Número de horas até a expiração desde a geração da imagem de resposta. Defina como 0 para sempre expirar a imagem de resposta imediatamente, o que desativa efetivamente o cache do cliente. Defina como -1 para marcar como *`never expire`*. Nesse caso, o servidor sempre retorna o status 304 (não modificado) em resposta a solicitações condicionais do GET sem verificar se o arquivo foi realmente alterado. Defina como -2 para usar o padrão fornecido por `attribute::Expiration`.

## Padrão {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` é usado se o campo não estiver presente, se o valor for -2 ou se o campo estiver vazio.

## Consulte também {#section-0e5e8595aad641c689726828712a8902}

[attribute::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7), [attribute::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d), [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
