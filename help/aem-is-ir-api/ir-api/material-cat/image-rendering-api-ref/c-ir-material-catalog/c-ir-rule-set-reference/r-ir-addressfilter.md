---
description: Elemento de filtro de endereço. Opcional em elementos <rule>. Substitui o atributo ClientAddressFilter quando a regra é aplicada.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# addressfilter{#addressfilter}

Elemento de filtro de endereço. Opcional em `<rule>` elementos. Substitui attribute::ClientAddressFilter quando a regra é aplicada.

## Atributos {#section-e7a0960f7f0045da91de37824aa4aeaa}

Nenhum.

## Dados {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Lista de endereços IP separados por vírgulas. Cada endereço individual pode incluir um sufixo de máscara de rede opcional para permitir a especificação de intervalos de endereço IP. Consulte [attribute::ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md) para obter detalhes.

## Descrição {#section-099b7839c4be40c68cbff29dad14e7d5}

O acesso a este catálogo de imagens pode ser restrito a um ou mais endereços IP específicos especificando-os em um elemento `<addressfilter>`. Um erro &quot;request refused&quot; é retornado ao cliente se o endereço IP do cliente não for compatível.

O acesso não é restrito se `<addressfilter>` estiver vazio ou não for especificado.

Se o `<expression>` no elemento `<rule>` estiver ausente ou vazio, o `<addressfilter>` será aplicado a todas as solicitações.

`localhost` sempre faz parte implicitamente da definição `ClientAddressFilter`, mesmo que não seja explicitamente especificado. As solicitações originadas de `localhost` nunca são rejeitadas, independentemente da especificação `ClientAddressFilter`.

## SeeaAlso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
