---
title: áspero
description: Rugosidade da superfície do material. Especifica a rugosidade relativa da superfície do material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
TQID: 'https://experienceleague.adobe.com/FhLagzJwQodPihSxkEyBl8zSnEU0gDq0zevixYMApUY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 182
ht-degree: 0%

---

# áspero{#rough}

Rugosidade da superfície do material. Especifica a rugosidade relativa da superfície do material.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Rugosidade da superfície (0 a 100%) ou -1 para selecionar a rugosidade padrão. </p> </td> 
 </tr> 
</table>

Usado para controlar o efeito de renderização da reflexão 3D. Valores de rugosidade mais baixos normalmente produzem efeitos de reflexão mais suaves; valores mais altos causam aleatoriedade e dispersão da imagem refletida.

Cada tipo de material ( `type=`) define um efeito de renderização de reflexão mínimo e máximo com base na rugosidade. Para alguns tipos de material (por exemplo, papel de parede), `rough=` tem impacto mínimo na aparência da reflexão, enquanto para outros tipos de material (por exemplo, pedra ou cerâmica), o efeito é substancialmente mais pronunciado.

`rough=-1` Define a rugosidade como um valor padrão interno do servidor (40% para tipos de material típicos).

## Propriedades {#section-515375758b254c80af576271bdb61bb8}

Atributo de material. Ignorado se a vinheta não tiver o recurso de reflexão 3D, se o objeto de destino não tiver geometria 3D associada a ele ou se o objeto de destino não estiver refletindo outros objetos na cena.

## Padrão {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` Se o material for baseado em uma entrada de catálogo, caso contrário, aproximadamente 40%.

## Consulte também {#section-d232fff7237443cc95c4bb50cb3d32bb}

[tipo=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [brilho=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)

