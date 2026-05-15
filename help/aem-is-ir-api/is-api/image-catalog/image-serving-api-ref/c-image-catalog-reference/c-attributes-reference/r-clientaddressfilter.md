---
description: Filtro de endereço IP do cliente. Permite a especificação de um ou mais endereços IP ou intervalos de endereços.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
TQID: 'https://experienceleague.adobe.com/cQT0eRo0amqhX76H3dNZakwlGsKt3-MAkIsRZytyREI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 0%

---

# ClientAddressFilter{#clientaddressfilter}

Filtro de endereço IP do cliente. Permite a especificação de um ou mais endereços IP ou intervalos de endereços.

Quando especificado, as solicitações para este catálogo de imagens originadas de um cliente em um endereço IP não listado são rejeitadas.

## Propriedades {#section-d785265988324af68835410c9ba54147}

Lista separada por vírgulas de endereços IP com máscaras de rede opcionais (a notação CIDR é usada):

`*`ipAddress`*` `[`/ *`netmask`*`]`&#42; `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> endereçoIP</span> </p> </td> 
  <td class="stentry"> <p>Endereço IP no formato <span class="varname"> ddd.ddd.ddd.ddd</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> máscara de rede</span> </p></td> 
  <td class="stentry"> <p>Máscara de rede (0 a 32). </p></td> 
 </tr> 
</table>

Esse atributo é ignorado quando uma regra de pré-processamento com um elemento `<addressfilter>` é aplicada.

## Padrão {#section-de26e8c9225745e985e4beac1f03f4f6}

Herdado de `default::AddressFilter` se não estiver definido ou se estiver vazio.

## Exemplos {#section-a955314d2b6a4213a16c12a8b18d8627}

Sem restrições de acesso: `0.0.0.0/0`

Conceder acesso a todos os endereços iniciando com 192: `192.0.0.0/8`

Conceder acesso aos 512 hosts com endereços entre 192.168.12.0 e 192.168.13.255: `192.168.12.0/23`

Conceder acesso a um único endereço IP: `192.168.2.117` ou `192.168.2.117/32`

## Consulte também {#section-4ea89a7d82e14a4a800487d2d8801465}

[addressfilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
