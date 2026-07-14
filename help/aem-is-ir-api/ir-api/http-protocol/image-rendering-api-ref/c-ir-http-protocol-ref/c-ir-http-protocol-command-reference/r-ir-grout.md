---
title: caldas de injeção
description: Cor e espessura da argamassa da telha. Simula a calda para telhas de cerâmica e pedra natural.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
TQID: 'https://experienceleague.adobe.com/FrYxcizVu3nXej1tt4QpX0AsLEylXTfwYRaSQP43HNI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 0%

---

# caldas de injeção {#grout}

Cor e espessura da argamassa da telha. Simula a calda para telhas de cerâmica e pedra natural.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cor </span> </span> </p> </td>
  <td class="stentry"> <p>Cor de argamassa (cinza ou RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> largura </span> </span> </p> </td>
  <td class="stentry"> <p>Espessura da argamassa; unidades de coordenadas de cena (normalmente polegadas) (real). </p> </td>
 </tr> 
</table>

Para o controle máximo da aparência da calda, aplicam-se os seguintes requisitos:

* O bloco deve ser quadrado ou retangular; nenhuma outra forma é suportada no momento.
* A imagem deve conter apenas um único bloco.
* A argamassa padrão na imagem (se houver) deve ter a mesma espessura em todas as quatro bordas.
* A espessura da calda padrão deve ser especificada no catálogo de materiais ( `catalog::GroutWidth`).

## Propriedades {#section-de78b678245b4ffda48097c345949e77}

Atributo de material. `*`cor`*` deve ser um valor de cor RGB. `*`width`*` deve ser um valor real 0 ou maior.

Ignorado se repetir = 4, 5, 7, 8, 9, 14 ou superior, ou quando especificado para materiais que não sejam texturas repetíveis.

## Padrão {#section-bfab3621f70b4489a21994ab11b20cc6}

Se `grout=` não for especificado, a argamassa da imagem não será modificada. Se `grout= *`color`*` for especificado, `*`width`*` assumirá `catalog::GroutWidth` como padrão.

## Consulte também {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valores de cor](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)

