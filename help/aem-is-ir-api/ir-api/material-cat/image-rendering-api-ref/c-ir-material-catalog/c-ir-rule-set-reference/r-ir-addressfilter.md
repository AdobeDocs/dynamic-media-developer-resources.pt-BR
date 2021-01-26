---
description: Elemento de filtro de endereço. Opcional em elementos <rule>. Substitui o atributo ClientAddressFilter quando a regra é aplicada.
seo-description: Elemento de filtro de endereço. Opcional em elementos <rule>. Substitui o atributo ClientAddressFilter quando a regra é aplicada.
seo-title: enderesfilter
solution: Experience Manager
title: enderesfilter
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e5702c6e-a49c-4da6-a29c-26e16bfdcad1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# enderesfilter{#addressfilter}

Elemento de filtro de endereço. Opcional nos elementos `<rule>`. Substitui o atributo::ClientAddressFilter quando a regra é aplicada.

## Atributos {#section-e7a0960f7f0045da91de37824aa4aeaa}

Nenhum.

## Dados {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Lista separada por vírgulas de endereços IP. Cada endereço individual pode incluir um sufixo opcional de máscara de rede para permitir a especificação de intervalos de endereço IP. Consulte ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)` para obter detalhes.

## Descrição {#section-099b7839c4be40c68cbff29dad14e7d5}

O acesso a esse catálogo de imagens pode ser restrito a um ou mais endereços IP específicos, especificando-os em um elemento `<addressfilter>`. Um erro de &quot;solicitação recusada&quot; será retornado ao cliente se o endereço IP do cliente não for correspondente.

O acesso não é restrito se `<addressfilter>` estiver vazio ou não for especificado.

Se `<expression>` no elemento `<rule>` estiver ausente ou vazio, `<addressfilter>` será aplicado a todas as solicitações.

`localhost` é sempre implicitamente parte da  `ClientAddressFilter` definição, mesmo que não seja explicitamente especificada. As solicitações originárias de `localhost` nunca são rejeitadas, independentemente da especificação `ClientAddressFilter`.

## SeeaTambém {#section-02056065e0c042e1b155b2f3e5b84ef7}

[atributo::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
