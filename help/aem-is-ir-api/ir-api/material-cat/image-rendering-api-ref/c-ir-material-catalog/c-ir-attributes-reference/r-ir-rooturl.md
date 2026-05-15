---
title: RootUrl
description: URL raiz para URLs de imagem relativos. Especifica a URL raiz para URLs de imagem relativas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
TQID: 'https://experienceleague.adobe.com/1wKgvbd1t4HyDlz-CTDkp2gQuryBJYfMyDG7SmVgNwE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 0%

---

# RootUrl{#rooturl}

URL raiz para URLs de imagem relativos. Especifica a URL raiz para URLs de imagem relativas. O `attribute::RootUrl` é usado em vez de `attribute::RootPath` quando um valor `src=` é delimitado por {curly braces}.

## Propriedades {#section-69cd0f71ea614770a8778c745d23197a}

Valor da string de texto. Caminho raiz absoluto do URL, incluindo o identificador de protocolo principal. Os seguintes protocolos são compatíveis: HTTP, HTTPS e FTP.

## Padrão {#section-7a81569728474725a70f3a2cc4d48e85}

Herdado de `default::RootUrl` se não estiver definido. Se definido, mas vazio, os URLs relativos não são suportados por este catálogo de materiais.

## Consulte também {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [atributo:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
