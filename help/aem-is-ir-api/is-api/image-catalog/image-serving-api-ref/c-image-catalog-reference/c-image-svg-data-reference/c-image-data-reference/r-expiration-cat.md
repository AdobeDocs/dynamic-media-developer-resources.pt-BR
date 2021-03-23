---
description: Expiração
solution: Experience Manager
title: Expiração
uuid: 5c9e5f76-c65f-4193-adf7-fb635fc5a071
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---


# Expiração{#expiration}

Usado para gerenciar o armazenamento em cache do cliente e do servidor proxy. O servidor calcula a hora/data de expiração dos dados de resposta HTTP adicionando esse valor à hora/data da transmissão.

Os navegadores gerenciam caches usando tempos de expiração de arquivos. Antes de passar uma solicitação para o servidor, o navegador verifica seu cache para ver se o arquivo já foi baixado. Nesse caso, e se o arquivo ainda não tiver expirado, o navegador enviará uma solicitação de GET condicional (por exemplo, com o campo If-Modified-Since definido no cabeçalho da solicitação) em vez de uma solicitação GET normal. O servidor tem a opção de responder com um status &quot;304&quot; e não transmitir a imagem. Em seguida, o navegador carrega o arquivo de seu cache. Isso pode aumentar substancialmente o desempenho geral para dados acessados com frequência.

A expiração é usada para estes tipos de resposta:

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

Determinados tipos de respostas (por exemplo, respostas de erro) são sempre marcadas para expiração imediata (ou marcadas como não armazenáveis em cache), enquanto outros (por exemplo, respostas de propriedade ou de imagem padrão) usam configurações de expiração especiais ( `attribute::NonImgExpiration` e `attribute::DefaultExpiration`).

## Propriedades {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

Número real, -2, -1 ou 0 ou maior. Número de horas até a expiração desde que a imagem de resposta foi gerada. Defina como 0 para sempre expirar a imagem de resposta imediatamente, o que efetivamente desativa o armazenamento em cache do cliente. Defina como -1 para marcar como *`never expire`*. Nesse caso, o servidor sempre retorna o status 304 (não modificado) em resposta a solicitações de GET condicionais sem verificar se o arquivo foi realmente alterado. Defina como -2 para usar o padrão fornecido por `attribute::Expiration`.

## Padrão {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` é usado se o campo não estiver presente, se o valor for -2 ou se o campo estiver vazio.

## Consulte também {#section-0e5e8595aad641c689726828712a8902}

[atributo::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7),  [atributo::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [atributo::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d),  [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
