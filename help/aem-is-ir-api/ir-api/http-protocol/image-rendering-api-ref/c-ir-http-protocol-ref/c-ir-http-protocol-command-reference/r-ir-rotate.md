---
title: girar
description: Ângulo de rotação do material. Define o ângulo de rotação dos materiais.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# girar{#rotate}

Ângulo de rotação do material. Define o ângulo de rotação dos materiais.

` rotate= *`ângulo`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> ângulo </span> </p> </td> 
  <td class="stentry"> <p>Ângulo de rotação em graus (real). </p> </td> 
 </tr> 
</table>

Girar os materiais de textura repetível (excluindo papéis de parede) em múltiplos de 45° quando aplicados a objetos planos ou objetos planos.

Girar materiais de textura repetíveis por ângulos arbitrários quando aplicados a Objetos Flowline e Sketch.

Girar materiais de decalque por ângulos arbitrários.

Ângulos positivos giram no sentido horário. A textura ou decalque é girada em torno do ponto de ancoragem ( `anchor=`); o ponto de ancoragem permanece alinhado com a origem do objeto de destino.

## Propriedades {#section-ad4d07897ca24f63af1a4062f8618e36}

Atributo de material. Ignorado por materiais de tratamento de cor sólida, papel de parede, armário e janela. *`angle`* Deve ser um múltiplo de 45 para texturas repetíveis, a menos que seja aplicado a Objetos Flowline ou Sketch.

## Padrão {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, sem rotação.

## Consulte também {#section-f73c00e9368b478dac1fd15bb4367a12}

[âncora=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
