---
description: Elemento de filtro de endereço. Opcional nos elementos <rule> e <pathrule>.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# addressfilter{#addressfilter}

Elemento de filtro de endereço. Opcional em elementos `<rule>` e `<pathrule>`.

Substitui `attribute::ClientAddressFilter` quando a regra é aplicada.

## Atributos {#section-31e9ad29e9934933ac154bccbc729172}

Nenhum.

## Dados {#section-c762bdfe425140d689ea5abf25e9a48a}

Lista de endereços IP separados por vírgulas. Cada endereço individual pode incluir um sufixo de máscara de rede opcional para permitir a especificação de intervalos de endereço IP. Consulte `attribute::ClientAddressFilter` para obter detalhes.

## Descrição {#section-d561b2485e004ef8a2085997d0f4bca6}

O acesso a este catálogo de imagens pode ser restrito a um ou mais endereços IP de cliente específicos especificando-os em um elemento `<addressfilter>`. Um erro &quot;request refused&quot; é retornado ao cliente se o endereço IP do cliente não for compatível.

O acesso não é restrito se `<addressfilter>` estiver vazio ou não for especificado.

Se o `<expression>` no elemento `<rule>` estiver ausente ou vazio, o `<addressfilter>` será aplicado a todas as solicitações.

## Consulte também {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
