---
description: Elemento de filtro de endereço. Opcional em elementos <rule>. Substitui o atributo ClientAddressFilter quando a regra é aplicada.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
TQID: 'https://experienceleague.adobe.com/583zFF80AMZnaF4C-RQpRQI684hRlPRCuwoMPHGJ6eg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 150
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
