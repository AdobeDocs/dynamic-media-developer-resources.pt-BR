---
description: Ângulo de rotação do material. Define o ângulo de rotação dos materiais.
seo-description: Ângulo de rotação do material. Define o ângulo de rotação dos materiais.
seo-title: girar
solution: Experience Manager
title: girar
uuid: 497cd8ea-c6a4-45d2-b5e0-0898ac00913d
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---


# rotate{#rotate}

Ângulo de rotação do material. Define o ângulo de rotação dos materiais.

` rotate= *`ângulo`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> ângulo  </span> </p> </td> 
  <td class="stentry"> <p>Ângulo de rotação em graus (real). </p> </td> 
 </tr> 
</table>

Girar os materiais de textura repetível (excluindo papéis de parede) em múltiplos de 45 graus quando aplicados a objetos planos ou objetos planos.

Girar materiais de textura repetíveis por ângulos arbitrários quando aplicados a Objetos Flowline e Sketch.

Girar materiais de decalque por ângulos arbitrários.

Ângulos positivos giram no sentido horário. A textura ou decalque é girada em torno do ponto de ancoragem ( `anchor=`); o ponto de ancoragem permanece alinhado com a origem do objeto de destino.

## Propriedades {#section-ad4d07897ca24f63af1a4062f8618e36}

Atributo de material. Ignorado por materiais de tratamento de cor sólida, papel de parede, armário e janela. *`angle`* deve ser um múltiplo de 45 para texturas repetíveis, a menos que seja aplicado a objetos Flowline ou Sketch.

## Padrão {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, sem rotação.

## Consulte também {#section-f73c00e9368b478dac1fd15bb4367a12}

[âncora=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
