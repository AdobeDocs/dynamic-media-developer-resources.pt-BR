---
description: Configurações avançadas de renderização. Especifica uma configuração de renderização avançada, a ser aplicada ao renderizar a seleção atual.
seo-description: Configurações avançadas de renderização. Especifica uma configuração de renderização avançada, a ser aplicada ao renderizar a seleção atual.
seo-title: rs
solution: Experience Manager
title: rs
topic: Scene7 Image Serving - Image Rendering API
uuid: 4ff7fcb4-a10a-4e82-80a1-edf79ae1f717
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# rs{#rs}

Configurações avançadas de renderização. Especifica uma configuração de renderização avançada, a ser aplicada ao renderizar a seleção atual.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Sequência de caracteres de configurações de renderização. </p></td> 
 </tr> 
</table>

Usado para ajustar a aparência da renderização. Use o recurso de renderização da Ferramenta de criação de vinheta (parte do pacote Scene7 Image Authoring) para criar strings de configurações de renderização.

## Propriedades {#section-9a2b2228789046658cb80eddf343af75}

Atributo material.

## Padrão {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Example {#section-47e4811882574441a4d517e42a35f352}

Depois de algum experimento na Criação de imagens, determina-se que o mascaramento com nitidez (USM) fornece a quantidade correta de nitidez para o aplicativo e o material em questão. A string de configurações de renderização que configura o USM é copiada para o `rs=` comando para usar com este material:

`…&rs=U2V20W50X2&…`

## Consulte também {#section-930116e735024a008c994547ba36ee40}

[catálogo::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
