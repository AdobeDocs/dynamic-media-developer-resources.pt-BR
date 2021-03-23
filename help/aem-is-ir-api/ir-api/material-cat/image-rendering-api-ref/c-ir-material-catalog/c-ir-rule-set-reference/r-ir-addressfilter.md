---
description: Elemento de filtro de endereço. Opcional em elementos <rule> . Substitui o atributo ClientAddressFilter quando a regra é aplicada.
seo-description: Elemento de filtro de endereço. Opcional em elementos <rule> . Substitui o atributo ClientAddressFilter quando a regra é aplicada.
seo-title: addressFilter
solution: Experience Manager
title: addressFilter
uuid: e5702c6e-a49c-4da6-a29c-26e16bfdcad1
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---


# address_filter{#addressfilter}

Elemento de filtro de endereço. Opcional em elementos `<rule>`. Substitui o atributo::ClientAddressFilter quando a regra é aplicada.

## Atributos {#section-e7a0960f7f0045da91de37824aa4aeaa}

Nenhum.

## Dados {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Lista de endereços IP separada por vírgulas. Cada endereço individual pode incluir um sufixo opcional de máscara de rede para permitir a especificação de intervalos de endereço IP. Consulte ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)` para obter detalhes.

## Descrição {#section-099b7839c4be40c68cbff29dad14e7d5}

O acesso a esse catálogo de imagem pode ser restrito a um ou mais endereços IP específicos, especificando-os em um elemento `<addressfilter>`. Um erro &quot;solicitação recusada&quot; é retornado ao cliente se o endereço IP do cliente não corresponder.

O acesso não é restrito se `<addressfilter>` estiver vazio ou não for especificado.

Se o `<expression>` no elemento `<rule>` estiver ausente ou vazio, o `<addressfilter>` será aplicado a todas as solicitações.

`localhost` sempre faz parte implicitamente da  `ClientAddressFilter` definição, mesmo que não tenha sido especificado explicitamente. As solicitações originárias de `localhost` nunca são rejeitadas, independentemente da especificação `ClientAddressFilter`.

## SeeaAlso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[atributo::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
