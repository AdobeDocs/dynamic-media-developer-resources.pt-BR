---
description: URL raiz para URLs de imagem relativos. Especifica o URL raiz de URLs de imagem relativos. O atributo RootUrl é usado em vez do atributo RootPath quando um src= valor é incluído por { chaves chaves }.
solution: Experience Manager
title: RootUrl *
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# RootUrl *{#rooturl}

URL raiz para URLs de imagem relativos. Especifica o URL raiz de URLs de imagem relativos. attribute::RootUrl é usado em vez do atributo::RootPath quando um src= valor é incluído por { chaves }.

## Propriedades {#section-69cd0f71ea614770a8778c745d23197a}

Valor da string de texto. Caminho raiz do URL absoluto, incluindo o identificador de protocolo à esquerda. Os seguintes protocolos são compatíveis: HTTP, HTTPS e FTP.

## Padrão {#section-7a81569728474725a70f3a2cc4d48e85}

Herdado de `default::RootUrl` se não estiver definido. Se definido, mas vazio, URLs relativos não são compatíveis com esse catálogo de materiais.

## Consulte também {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`,  [attribute:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
