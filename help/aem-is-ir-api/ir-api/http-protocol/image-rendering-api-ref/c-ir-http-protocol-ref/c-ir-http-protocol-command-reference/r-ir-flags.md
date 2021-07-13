---
description: Aplique sinalizadores. Especifica opções de renderização adicionais.
solution: Experience Manager
title: sinalizadores
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
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
