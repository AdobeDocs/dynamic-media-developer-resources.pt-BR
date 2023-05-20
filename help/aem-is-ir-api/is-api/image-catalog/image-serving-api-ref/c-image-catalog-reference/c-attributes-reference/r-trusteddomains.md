---
description: domínios da Web de aplicativos do Flash. Os aplicativos do Flash Adobe podem exigir acesso às propriedades das imagens fornecidas com fmt=swf ou fmt=swf3.
solution: Experience Manager
title: DomíniosConfiáveis
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# DomíniosConfiáveis{#trusteddomains}

domínios da Web de aplicativos do Flash. Os aplicativos do Flash Adobe podem exigir acesso às propriedades das imagens fornecidas com fmt=swf ou fmt=swf3.

O swf deve conceder acesso explicitamente registrando o nome dos domínios de aplicativo nos quais ele confia.

## Propriedades {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

String contendo uma lista separada por vírgulas de nomes de domínio da Web. Se estiverem vazios, os aplicativos devem ser veiculados no mesmo domínio que a Renderização de imagem para acessar as propriedades das imagens em respostas formatadas em swf.

## Padrão {#section-5c52ed3c7310488380f5a6f9540bf981}

Herdado de `default::TrustedDomains` se não estiver presente.

## Consulte também {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
