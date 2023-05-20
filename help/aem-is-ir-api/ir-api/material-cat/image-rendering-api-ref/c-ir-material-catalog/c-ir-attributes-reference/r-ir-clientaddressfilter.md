---
title: ClientAddressFilter
description: Filtro de endereço IP do cliente. Permite a especificação de um ou mais endereços IP ou intervalos de endereços.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# ClientAddressFilter{#clientaddressfilter}

Filtro de endereço IP do cliente. Permite a especificação de um ou mais endereços IP ou intervalos de endereços.

Quando especificado, as solicitações para este catálogo de imagens originadas de um cliente em um endereço IP não listado são rejeitadas. `localhost` sempre faz parte implicitamente do `ClientAddressFilter` definição, mesmo que não seja explicitamente especificada. Solicitações originadas de `localhost` nunca são rejeitados, independentemente da `ClientAddressFilter` especificação.

## Propriedades {#section-21a2992f108d42fb8660c0d65aa61e13}

Lista separada por vírgulas de endereços IP com máscaras de rede opcionais ([Notação CIDR](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) é usado):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* Endereço IP em *[!DNL ddd.ddd.ddd.ddd]* formato

* *[!DNL netmask]* máscara de rede (0 a 32)

Esse atributo é ignorado quando uma regra de pré-processamento com um `<addressfilter>` elemento é aplicado.

## Padrão {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Herdado de `default::AddressFilter` se não estiver definido ou se estiver vazio.

## Exemplos {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Sem restrições de acesso: `0.0.0.0/0`
* Conceder acesso a todos os endereços que comecem com `192: 192.0.0.0/8`
* Conceder acesso aos 512 hosts com endereços entre `192.168.12.0` e `192.168.13.255: 192.168.12.0/23`

* Conceder acesso a um único endereço IP: `192.168.2.117` ou `192.168.2.117/32`

## Consulte também {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
