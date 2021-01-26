---
description: Filtro de endereço IP do cliente. Permite a especificação de um ou mais endereços IP ou intervalos de endereços.
seo-description: Filtro de endereço IP do cliente. Permite a especificação de um ou mais endereços IP ou intervalos de endereços.
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b68f527b-7fa7-43e3-9517-57a6c3700b06
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---


# ClientAddressFilter{#clientaddressfilter}

Filtro de endereço IP do cliente. Permite a especificação de um ou mais endereços IP ou intervalos de endereços.

Quando especificado, as solicitações para este catálogo de imagens que se originam de um cliente em um endereço IP não listado serão rejeitadas. `localhost` é sempre implicitamente parte da  `ClientAddressFilter` definição, mesmo que não seja explicitamente especificada. As solicitações originárias de `localhost` nunca são rejeitadas, independentemente da especificação `ClientAddressFilter`.

## Propriedades {#section-21a2992f108d42fb8660c0d65aa61e13}

Lista separada por vírgulas de endereços IP com máscaras de rede opcionais ([notação CIDR](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) é usada):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* Endereço IP no  *[!DNL ddd.ddd.ddd.ddd]* formato

* *[!DNL netmask]* máscara de rede (0...32)

Este atributo é ignorado quando uma regra de pré-processamento com um elemento `<addressfilter>` é aplicada.

## Padrão {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Herdado de `default::AddressFilter` se não estiver definido ou se estiver vazio.

## Exemplos {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Sem restrições de acesso: `0.0.0.0/0`
* Conceder acesso a todos os endereços começando com `192: 192.0.0.0/8`
* Conceder acesso aos 512 hosts com endereços entre `192.168.12.0` e `192.168.13.255: 192.168.12.0/23`

* Conceder acesso a um único endereço IP: `192.168.2.117` ou `192.168.2.117/32`

## Consulte também {#section-6198780c7b3045aabd211eefb38bc565}

[enderesfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
