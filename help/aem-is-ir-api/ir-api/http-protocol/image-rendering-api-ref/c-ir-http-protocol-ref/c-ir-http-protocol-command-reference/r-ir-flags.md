---
title: sinalizadores
description: Aplicar sinalizadores. Especifica opções de renderização adicionais.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
TQID: 'https://experienceleague.adobe.com/tdbtQIxutlPSPRm4vGWCQLM8veyivWfabKos9YbvfYg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 0%

---

# sinalizadores {#flags}

Aplicar sinalizadores. Especifica opções de renderização adicionais.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Valor do sinalizador. </p></td> 
 </tr> 
</table>

Atualmente usado apenas para materiais de gabinete.

`flags=0` (padrão) Renderiza gabinetes superiores com portas sólidas.

`flags=1` Renderiza armários superiores com portas de vidro (se a vinheta foi criada com portas de vidro).

## Propriedades {#section-a2b00d7bb15e449ea85178acb92d8285}

Atributo de material. Ignorado se não for um material de gabinete, ou se o objeto de gabinete de destino não permitir portas de vidro.

## Padrão {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` Sem portas de vidro.
