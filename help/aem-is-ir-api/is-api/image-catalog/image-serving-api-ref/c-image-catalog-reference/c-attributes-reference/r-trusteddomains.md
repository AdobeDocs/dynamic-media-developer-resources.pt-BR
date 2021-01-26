---
description: Domínios da Web do aplicativo de Flash. Os aplicativos de Flash podem exigir acesso às propriedades de imagens fornecidas com fmt=swf ou fmt=swf3.
seo-description: Domínios da Web do aplicativo de Flash. Os aplicativos de Flash podem exigir acesso às propriedades de imagens fornecidas com fmt=swf ou fmt=swf3.
seo-title: TrustedDomains
solution: Experience Manager
title: TrustedDomains
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 1d056d68-b699-413c-897c-8612444735c5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# TrustedDomains{#trusteddomains}

Domínios da Web do aplicativo de Flash. Os aplicativos de Flash podem exigir acesso às propriedades de imagens fornecidas com fmt=swf ou fmt=swf3.

O swf deve conceder acesso explicitamente registrando o nome dos domínios de aplicativo em que confia.

## Propriedades {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Sequência que contém uma lista separada por vírgulas de nomes de domínio da Web. Se estiverem vazios, os aplicativos devem ser fornecidos do mesmo domínio que a Renderização de imagem para que possam acessar as propriedades das imagens em respostas formatadas em swf.

## Padrão {#section-5c52ed3c7310488380f5a6f9540bf981}

Herdado de `default::TrustedDomains` se não estiver presente.

## Consulte também {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
