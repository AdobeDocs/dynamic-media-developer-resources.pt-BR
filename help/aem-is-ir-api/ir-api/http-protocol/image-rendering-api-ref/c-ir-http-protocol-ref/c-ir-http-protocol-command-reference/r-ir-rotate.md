---
description: Ângulo de rotação do material. Define o ângulo de rotação dos materiais.
seo-description: Ângulo de rotação do material. Define o ângulo de rotação dos materiais.
seo-title: girar
solution: Experience Manager
title: girar
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 497cd8ea-c6a4-45d2-b5e0-0898ac00913d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '134'
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

Gire materiais de textura repetíveis (exceto papéis de parede) em múltiplos de 45 graus quando aplicados a Objetos Simples ou Objetos Planos.

Gire materiais de textura repetíveis por ângulos arbitrários quando aplicados a objetos de linha flutuante e de rascunho.

Gire materiais de decalque por ângulos arbitrários.

Ângulos positivos giram no sentido horário. A textura ou o decal é girado em torno do ponto de ancoragem ( `anchor=`); o ponto de ancoragem permanece alinhado à origem do objeto de público alvo.

## Propriedades {#section-ad4d07897ca24f63af1a4062f8618e36}

Atributo material. Ignorados por materiais de tratamento de cor sólida, papel de parede, armário e janelas. *`angle`* deve ser um múltiplo de 45 para texturas repetíveis, a menos que seja aplicado a objetos de linha flutuante ou de rascunho.

## Padrão {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, sem rotação.

## Consulte também {#section-f73c00e9368b478dac1fd15bb4367a12}

[âncora=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
