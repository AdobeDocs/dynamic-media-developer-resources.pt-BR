---
description: Configurações avançadas de renderização. Especifica uma configuração de renderização avançada, a ser aplicada ao renderizar a seleção atual.
seo-description: Configurações avançadas de renderização. Especifica uma configuração de renderização avançada, a ser aplicada ao renderizar a seleção atual.
seo-title: rs
solution: Experience Manager
title: rs
uuid: 4ff7fcb4-a10a-4e82-80a1-edf79ae1f717
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

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

Usado para ajustar a aparência da renderização. Use o recurso de renderização da Ferramenta de criação de vinhetas (parte do pacote Dynamic Media Image Authoring) para criar cadeias de caracteres de configurações de renderização.

## Propriedades {#section-9a2b2228789046658cb80eddf343af75}

Atributo de material.

## Padrão {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Exemplo {#section-47e4811882574441a4d517e42a35f352}

Após algumas experiências na Criação de Imagens, determina-se que o mascaramento com nitidez (USM) fornece a quantidade correta de nitidez para o aplicativo e o material em questão. A cadeia de caracteres de configurações de renderização que configura o USM é copiada para o comando `rs=` para usar com este material:

`…&rs=U2V20W50X2&…`

## Consulte também {#section-930116e735024a008c994547ba36ee40}

[catálogo::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
