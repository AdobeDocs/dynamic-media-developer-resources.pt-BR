---
description: Filtro de endereço IP do cliente. Permite a especificação de um ou mais endereços IP ou intervalos de endereços.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '133'
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
