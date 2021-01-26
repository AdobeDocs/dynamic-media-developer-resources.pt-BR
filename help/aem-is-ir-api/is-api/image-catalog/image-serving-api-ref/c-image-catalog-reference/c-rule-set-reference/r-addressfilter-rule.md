---
description: Elemento de filtro de endereço. Opcional nos elementos <rule> e <pathrule>.
seo-description: Elemento de filtro de endereço. Opcional nos elementos <rule> e <pathrule>.
seo-title: enderesfilter
solution: Experience Manager
title: enderesfilter
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 677eb19f-fd1a-4f74-8d55-6045baf01bf5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# enderesfilter{#addressfilter}

Elemento de filtro de endereço. Opcional nos elementos `<rule>` e `<pathrule>`.

Substitui `attribute::ClientAddressFilter` quando a regra é aplicada.

## Atributos {#section-31e9ad29e9934933ac154bccbc729172}

Nenhum.

## Dados {#section-c762bdfe425140d689ea5abf25e9a48a}

Lista separada por vírgulas de endereços IP. Cada endereço individual pode incluir um sufixo opcional de máscara de rede para permitir a especificação de intervalos de endereço IP. Consulte `attribute::ClientAddressFilter` para obter detalhes.

## Descrição {#section-d561b2485e004ef8a2085997d0f4bca6}

O acesso a este catálogo de imagens pode ser restrito a um ou mais endereços IP do cliente específicos ao especificá-los em um elemento `<addressfilter>`. Um erro de &quot;solicitação recusada&quot; será retornado ao cliente se o endereço IP do cliente não for correspondente.

O acesso não é restrito se `<addressfilter>` estiver vazio ou não for especificado.

Se `<expression>` no elemento `<rule>` estiver ausente ou vazio, `<addressfilter>` será aplicado a todas as solicitações.

## Consulte também {#section-6f51ec2218d9450bb7642f9fdad1988a}

[atributo::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
