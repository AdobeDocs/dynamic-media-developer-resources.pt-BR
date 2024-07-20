---
title: Expiração
description: Tempo de vida do cache do cliente. Número de horas até a expiração. Usado para gerenciar o cache do cliente e do servidor proxy.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Expiração{#expiration}

Tempo de vida do cache do cliente. Número de horas até a expiração. Usado para gerenciar o cache do cliente e do servidor proxy.

O servidor calcula a data/hora de expiração dos dados de resposta NTTP adicionando esse valor à data/hora de transmissão.

Os navegadores gerenciam caches usando tempos de expiração de arquivos. Antes de passar uma solicitação para o servidor, o navegador verifica seu cache para ver se o arquivo já foi baixado. Em caso positivo, e se o arquivo ainda não tiver expirado, o navegador enviará uma solicitação condicional GET (por exemplo, com o cabeçalho de solicitação HTTP If-Modified-Since ) em vez de uma solicitação GET normal. O servidor tem a opção de responder com um status &quot;304&quot; e não transmitir a imagem. Em seguida, o navegador simplesmente carrega o arquivo do cache. Isso pode aumentar substancialmente o desempenho geral dos dados acessados com frequência.

O servidor define o cabeçalho de resposta HTTP expires para a data/hora atual mais o menor dos valores vignette::Expiration e all catalog::Expiration para a vinheta e todos os materiais envolvidos na operação de renderização.

A expiração é definida principalmente para respostas de dados de imagem. Determinados tipos de respostas são sempre marcados para expiração imediata (ou marcados como não armazenáveis em cache), incluindo todas as respostas de erro ou respostas de propriedade.

## Propriedades {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

Número real, -2, -1, 0 ou maior. Número de horas até a expiração desde a geração da imagem de resposta. Defina como 0 para sempre expirar a imagem de resposta imediatamente, o que desativa efetivamente o cache do cliente. Defina como -1 para marcar como `never expire`. Nesse caso, o servidor sempre retorna o status 304 (não modificado) em resposta a solicitações condicionais `GET` sem verificar se o arquivo realmente foi alterado. Defina como -2 para usar o padrão fornecido por `attribute::Expiration`.

## Padrão {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` é usado se o campo não estiver presente, se o valor for -2 ou se o campo estiver vazio.

## Consulte também {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
