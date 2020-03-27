---
description: Cor e espessura da argila do bloco. Simula argila para azulejos cerâmicos e naturais.
seo-description: Cor e espessura da argila do bloco. Simula argila para azulejos cerâmicos e naturais.
seo-title: argila
solution: Experience Manager
title: argila
topic: Scene7 Image Serving - Image Rendering API
uuid: 00069004-40f2-4ab6-85d8-ca197b7bef69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# argila{#grout}

Cor e espessura da argila do bloco. Simula argila para azulejos cerâmicos e naturais.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cor </span></span> </p> </td> 
  <td class="stentry"> <p>Cor do grupo (cinza ou RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> largura </span></span> </p> </td> 
  <td class="stentry"> <p>Espessura do grupo; unidades de coordenadas de cena (tipicamente polegadas) (real). </p> </td> 
 </tr> 
</table>

Para o controlo máximo da aparência do caldo de injeção, aplicam-se os seguintes requisitos:

* O mosaico deve ser quadrado ou retangular; nenhuma outra forma é suportada neste momento.
* A imagem deve conter apenas um bloco gráfico.
* A argila padrão na imagem (se houver) deve ter exatamente a mesma espessura em todas as quatro bordas.
* A espessura da argila padrão deve ser especificada no catálogo de materiais ( `catalog::GroutWidth`).

## Propriedades {#section-de78b678245b4ffda48097c345949e77}

Atributo material. ` *`color`*` deve ser um valor de cor RGB. ` *`width`*` deve ser um valor real 0 ou maior.

Ignorado se repetir = 4, 5, 7, 8, 9, 14 ou superior, ou quando especificado para materiais que não sejam texturas repetíveis.

## Padrão {#section-bfab3621f70b4489a21994ab11b20cc6}

Se não `grout=` for especificado, o gráfico na imagem não será modificado. Se a ` grout= *`cor`*` for especificada, a ` *`largura`*` assumirá o padrão `catalog::GroutWidth`.

## Consulte também {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valores de cor](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
