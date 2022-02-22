---
title: copião
description: Rugosidade da superfície do material. Especifica a rugosidade relativa da superfície do material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# copião{#rough}

Rugosidade da superfície do material. Especifica a rugosidade relativa da superfície do material.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Agitação superficial (0...100%) ou -1 para selecionar a rugosidade padrão. </p> </td> 
 </tr> 
</table>

Usado para controlar o efeito de renderização do reflexo 3D. Os valores de rugosidade mais baixos produzem normalmente efeitos de reflexão mais suaves. valores mais altos causam aleatoriedade e dispersão da imagem refletida.

Cada tipo de material ( `type=`) define um efeito de renderização de reflexo mínimo e máximo com base em rugosidade. Para alguns tipos de materiais (por exemplo, papel de parede), `rough=` tenha um impacto mínimo no aspecto da reflexão, enquanto para outros tipos de materiais (por exemplo, pedra ou cerâmica) o efeito é substancialmente mais pronunciado.

`rough=-1` Define a rugosidade para um valor padrão interno do servidor (40% para tipos de materiais típicos).

## Propriedades {#section-515375758b254c80af576271bdb61bb8}

Atributo de material. Ignorado se a vinheta não tiver nenhum recurso de reflexão 3D, se o objeto de destino não tiver geometria 3D associada a ela ou se o objeto de destino não estiver refletindo nenhum outro objeto na cena.

## Padrão {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` Se o material for baseado em uma entrada de catálogo, caso contrário, aproximadamente 40%.

## Consulte também {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [brilho=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
