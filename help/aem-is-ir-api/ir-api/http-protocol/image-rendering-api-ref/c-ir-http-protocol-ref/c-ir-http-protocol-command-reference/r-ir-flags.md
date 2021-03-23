---
description: Aplique sinalizadores. Especifica opções de renderização adicionais.
seo-description: Aplique sinalizadores. Especifica opções de renderização adicionais.
seo-title: sinalizadores
solution: Experience Manager
title: sinalizadores
uuid: 43ed24fe-461e-4973-aa44-8fba66668e6f
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---


# sinalizadores{#flags}

Aplique sinalizadores. Especifica opções de renderização adicionais.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Valor do sinalizador. </p></td> 
 </tr> 
</table>

Atualmente usado apenas para materiais de gabinete.

`flags=0` (padrão) renderiza os armários superiores com portas sólidas.

`flags=1` A gaveta deve ser fabricada com portas de vidro (se a vinheta tiver sido criada com portas de vidro).

## Propriedades {#section-a2b00d7bb15e449ea85178acb92d8285}

Atributo de material. Ignorado se não for um material do gabinete ou se o objeto do gabinete de destino não permitir portas de vidro.

## Padrão {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` sem portas de vidro.
