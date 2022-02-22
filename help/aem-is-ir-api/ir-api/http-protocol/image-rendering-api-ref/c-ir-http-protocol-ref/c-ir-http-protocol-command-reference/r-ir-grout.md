---
title: caldo
description: Cor e espessura do caldo de mosaico. Simula o caldo para azulejos de pedra cerâmica e natural.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---

# caldo {#grout}

Cor e espessura do caldo de mosaico. Simula o caldo para azulejos de pedra cerâmica e natural.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color </span> </span> </p> </td>
  <td class="stentry"> <p>Cor de grupo (cinza ou RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> largura </span> </span> </p> </td>
  <td class="stentry"> <p>Espessura do grupo; unidades de coordenadas de cena (tipicamente polegadas) (real). </p> </td>
 </tr> 
</table>

Para o controlo máximo da aparência do caldo de injeção, aplicam-se os seguintes requisitos:

* O mosaico deve ser quadrado ou retangular; nenhuma outra forma é suportada atualmente.
* A imagem deve conter apenas um bloco.
* O gráfico padrão na imagem (se houver) deve ter a mesma espessura em todas as quatro bordas.
* A espessura da calota predefinida deve ser especificada no catálogo de materiais ( `catalog::GroutWidth`).

## Propriedades {#section-de78b678245b4ffda48097c345949e77}

Atributo de material. `*`color`*` Deve ser um valor de cor RGB. `*`largura`*` deve ser um valor real 0 ou maior.

Ignorado se repetir = 4, 5, 7, 8, 9, 14 ou superior, ou quando especificado para materiais que não texturas repetíveis.

## Padrão {#section-bfab3621f70b4489a21994ab11b20cc6}

If `grout=` não for especificado, o grout na imagem não será modificado. If `grout= *`color`*` é especificado, `*`largura`*` o padrão é `catalog::GroutWidth`.

## Consulte também {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valores de cor](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
