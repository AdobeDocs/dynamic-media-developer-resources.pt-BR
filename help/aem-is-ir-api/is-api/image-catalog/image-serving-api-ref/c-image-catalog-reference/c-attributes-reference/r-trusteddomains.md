---
description: Domínios da Web do aplicativo Flash. Os aplicativos de Flash Adobe podem exigir acesso às propriedades de imagens fornecidas com fmt=swf ou fmt=swf3.
solution: Experience Manager
title: TrustedDomains
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# TrustedDomains{#trusteddomains}

Domínios da Web do aplicativo Flash. Os aplicativos de Flash Adobe podem exigir acesso às propriedades de imagens fornecidas com fmt=swf ou fmt=swf3.

O swf deve conceder acesso explicitamente, registrando o nome dos domínios de aplicativo em que confia.

## Propriedades {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Sequência de caracteres contendo uma lista separada por vírgulas de nomes de domínio da Web. Se estiverem vazios, os aplicativos devem ser veiculados a partir do mesmo domínio que a Renderização de imagem para que seja possível acessar as propriedades das imagens em respostas formatadas em swf.

## Padrão {#section-5c52ed3c7310488380f5a6f9540bf981}

Herdado de `default::TrustedDomains` se não estiver presente.

## Consulte também {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
