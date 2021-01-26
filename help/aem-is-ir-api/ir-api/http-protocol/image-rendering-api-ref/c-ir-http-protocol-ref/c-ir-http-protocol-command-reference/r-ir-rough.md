---
description: Rugosidade da superfície do material. Especifica a rugosidade relativa da superfície do material.
seo-description: Rugosidade da superfície do material. Especifica a rugosidade relativa da superfície do material.
seo-title: grosso
solution: Experience Manager
title: grosso
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d3b4ece1-cc2a-4012-ad81-2f313d3a370b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---


# bruços{#rough}

Rugosidade da superfície do material. Especifica a rugosidade relativa da superfície do material.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Aspereza da superfície (0,100%) ou -1 para selecionar a aspereza padrão. </p> </td> 
 </tr> 
</table>

Usado para controlar o efeito de renderização de reflexo 3D. Valores de rugosidade mais baixos normalmente produzem efeitos de reflexão mais suaves. valores mais altos causam aleatoriedade e dispersão da imagem refletida.

Cada tipo de material ( `type=`) define um efeito de renderização mínimo e máximo de reflexão com base na rugosidade. Para alguns tipos de materiais (por exemplo, papel de parede), `rough=` quase não tem qualquer impacto no aspecto da reflexão, enquanto para outros tipos de materiais (por exemplo, pedra ou cerâmica) o efeito é substancialmente mais pronunciado.

`rough=-1` define a rugosidade como um valor padrão interno do servidor (40% para tipos de material típicos).

## Propriedades {#section-515375758b254c80af576271bdb61bb8}

Atributo material. Ignorado se a vinheta não tiver nenhum recurso de reflexão 3D, se o objeto do público alvo não tiver uma geometria 3D associada a ela ou se o objeto do público alvo não estiver refletindo nenhum outro objeto na cena.

## Padrão {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` se o material for baseado em uma entrada de catálogo, caso contrário, aproximadamente 40%.

## Consulte também {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) ,  [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
