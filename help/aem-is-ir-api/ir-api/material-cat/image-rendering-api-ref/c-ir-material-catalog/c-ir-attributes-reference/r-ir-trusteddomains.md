---
description: Domínios da Web do aplicativo Flash. Os aplicativos Adobe Flash podem exigir acesso às propriedades de imagens entregues no formato swf. O swf deve conceder acesso explicitamente, registrando o nome do(s) domínio(s) do aplicativo em que confia.
solution: Experience Manager
title: TrustedDomains *
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# TrustedDomains *{#trusteddomains}

Domínios da Web do aplicativo Flash. Os aplicativos Adobe Flash podem exigir acesso às propriedades de imagens entregues no formato swf. O swf deve conceder acesso explicitamente, registrando o nome do(s) domínio(s) do aplicativo em que confia.

## Propriedades {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Sequência de caracteres contendo uma lista separada por vírgulas de nomes de domínio da Web. Se estiverem vazios, os aplicativos devem ser veiculados a partir do mesmo domínio que a Renderização de imagem para que seja possível acessar as propriedades das imagens em respostas formatadas em [!DNL swf].

## Padrão {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Herdado de `default::TrustedDomains` se não estiver presente.

## Consulte também {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`,  [atributo::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
