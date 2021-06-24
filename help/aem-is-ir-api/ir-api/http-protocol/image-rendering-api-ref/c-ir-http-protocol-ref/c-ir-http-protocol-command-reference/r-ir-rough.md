---
description: Rugosidade da superfície do material. Especifica a rugosidade relativa da superfície do material.
solution: Experience Manager
title: copião
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# copião{#rough}

Rugosidade da superfície do material. Especifica a rugosidade relativa da superfície do material.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Agitação superficial (0...100%) ou -1 para selecionar a rugosidade padrão. </p> </td> 
 </tr> 
</table>

Usado para controlar o efeito de renderização do reflexo 3D. Os valores de rugosidade mais baixos produzem normalmente efeitos de reflexão mais suaves. valores mais altos causam aleatoriedade e dispersão da imagem refletida.

Cada tipo de material ( `type=`) define um efeito de renderização mínimo e máximo de reflexão com base na rugosidade. Para alguns tipos de materiais (por exemplo, papel de parede), `rough=` quase não tem qualquer impacto no aspecto do reflexo, enquanto para outros tipos de materiais (por exemplo, pedra ou cerâmica) o efeito é substancialmente mais pronunciado.

`rough=-1` define a rugosidade como um valor padrão interno do servidor (40% para tipos de materiais típicos).

## Propriedades {#section-515375758b254c80af576271bdb61bb8}

Atributo de material. Ignorado se a vinheta não tiver nenhum recurso de reflexão 3D, se o objeto de destino não tiver geometria 3D associada a ela ou se o objeto de destino não estiver refletindo nenhum outro objeto na cena.

## Padrão {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` se o material for baseado em uma entrada de catálogo, caso contrário, aproximadamente 40%.

## Consulte também {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) ,  [brilho=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
