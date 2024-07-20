---
title: RootUrl
description: URL raiz para URLs de imagem relativos. Especifica a URL raiz para URLs de imagem relativas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# RootUrl{#rooturl}

URL raiz para URLs de imagem relativos. Especifica a URL raiz para URLs de imagem relativas. O `attribute::RootUrl` é usado em vez de `attribute::RootPath` quando um valor `src=` é delimitado por { chaves }.

## Propriedades {#section-69cd0f71ea614770a8778c745d23197a}

Valor da string de texto. Caminho raiz absoluto do URL, incluindo o identificador de protocolo principal. Os seguintes protocolos são compatíveis: HTTP, HTTPS e FTP.

## Padrão {#section-7a81569728474725a70f3a2cc4d48e85}

Herdado de `default::RootUrl` se não estiver definido. Se definido, mas vazio, os URLs relativos não são suportados por este catálogo de materiais.

## Consulte também {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [atributo:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
