---
description: Aplique sinalizadores. Especifica opções de renderização adicionais.
seo-description: Aplique sinalizadores. Especifica opções de renderização adicionais.
seo-title: sinalizadores
solution: Experience Manager
title: sinalizadores
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 43ed24fe-461e-4973-aa44-8fba66668e6f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---


# flags{#flags}

Aplique sinalizadores. Especifica opções de renderização adicionais.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Sinalizar valor. </p></td> 
 </tr> 
</table>

Atualmente usado apenas para materiais de gabinete.

`flags=0` (padrão) renderiza gabinetes superiores com portas sólidas.

`flags=1` forma as caixas superiores com portas de vidro (se a vinheta tiver sido criada com portas de vidro).

## Propriedades {#section-a2b00d7bb15e449ea85178acb92d8285}

Atributo material. Ignorado se não for um material do gabinete ou se o objeto do gabinete do público alvo não permitir portas de vidro.

## Padrão {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` sem portas de vidro.
