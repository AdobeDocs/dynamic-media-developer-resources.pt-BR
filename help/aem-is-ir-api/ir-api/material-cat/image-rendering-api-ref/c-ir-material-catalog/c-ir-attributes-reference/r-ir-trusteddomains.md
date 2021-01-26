---
description: Domínios da Web do aplicativo de Flash. Os aplicativos de Flash Adobe podem exigir acesso às propriedades de imagens entregues no formato swf. O swf deve conceder acesso explicitamente registrando o nome dos domínios de aplicativo em que confia.
seo-description: Domínios da Web do aplicativo de Flash. Os aplicativos de Flash Adobe podem exigir acesso às propriedades de imagens entregues no formato swf. O swf deve conceder acesso explicitamente registrando o nome dos domínios de aplicativo em que confia.
seo-title: TrustedDomains *
solution: Experience Manager
title: TrustedDomains *
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c50180b1-9af7-45f1-878f-59f41f9958ae
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# TrustedDomains *{#trusteddomains}

Domínios da Web do aplicativo de Flash. Os aplicativos de Flash Adobe podem exigir acesso às propriedades de imagens entregues no formato swf. O swf deve conceder acesso explicitamente registrando o nome dos domínios de aplicativo em que confia.

## Propriedades {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Sequência que contém uma lista separada por vírgulas de nomes de domínio da Web. Se estiverem vazios, os aplicativos devem ser fornecidos do mesmo domínio que a Renderização de imagem para que possam acessar as propriedades das imagens em respostas formatadas em [!DNL swf].

## Padrão {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Herdado de `default::TrustedDomains` se não estiver presente.

## Consulte também {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`,  [atributo::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
