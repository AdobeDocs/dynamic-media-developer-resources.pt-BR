---
description: Elemento de filtro de endereço. Opcional em <rule> elementos. Substitui o atributo ClientAddressFilter quando a regra é aplicada.
solution: Experience Manager
title: addressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# addressFilter{#addressfilter}

Elemento de filtro de endereço. Opcional em `<rule>` elementos. Substitui o atributo::ClientAddressFilter quando a regra é aplicada.

## Atributos {#section-e7a0960f7f0045da91de37824aa4aeaa}

Nenhum.

## Dados {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Lista de endereços IP separada por vírgulas. Cada endereço individual pode incluir um sufixo opcional de máscara de rede para permitir a especificação de intervalos de endereço IP. Consulte [atributo::ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md) para obter detalhes.

## Descrição {#section-099b7839c4be40c68cbff29dad14e7d5}

O acesso a este catálogo de imagens pode ser restrito a um ou mais endereços IP específicos, especificando-os em um `<addressfilter>` elemento. Um erro &quot;solicitação recusada&quot; é retornado ao cliente se o endereço IP do cliente não corresponder.

O acesso não é restrito se `<addressfilter>` está vazio ou não foi especificado.

Se a variável `<expression>` no `<rule>` estiver ausente ou vazio, o elemento `<addressfilter>` é aplicada a todas as solicitações.

`localhost` é sempre implicitamente parte do `ClientAddressFilter` definição, mesmo que não especificada explicitamente. Pedidos originários de `localhost` nunca são rejeitadas, independentemente do `ClientAddressFilter` especificação.

## SeeaAlso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[atributo::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
