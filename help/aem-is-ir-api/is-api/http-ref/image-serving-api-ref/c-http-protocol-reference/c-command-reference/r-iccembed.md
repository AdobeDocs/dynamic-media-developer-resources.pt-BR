---
title: iccEmbed
description: Incorporar perfil de cor. Especifica se o perfil de cores ICC de trabalho ou o perfil especificado com icc= deve ser incorporado na imagem de resposta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc5637f6-5452-4bfb-bf30-def6f153f4ad
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# iccEmbed{#iccembed}

Incorporar perfil de cor. Especifica se o perfil de cores ICC de trabalho ou o perfil especificado com icc= deve ser incorporado na imagem de resposta.

`iccEmbed=0|1`

## Propriedades {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Solicitar atributo. Ignorado se nenhum perfil estiver disponível para incorporação.

## Padrão {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`, para nenhuma incorporação de perfis ICC em imagens de saída. Ignorado se o formato de imagem de saída não suportar a incorporação de perfis ICC.

Consulte [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) para obter detalhes.

## Consulte também {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) , [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
