---
description: Aprimoramento de material padrão. Define o modo padrão de nitidez do material caso um registro de catálogo específico não contenha um valor de Sharp de catálogo válido.
seo-description: Aprimoramento de material padrão. Define o modo padrão de nitidez do material caso um registro de catálogo específico não contenha um valor de Sharp de catálogo válido.
seo-title: Nitidez
solution: Experience Manager
title: Nitidez
uuid: f6a6101c-3d9e-4557-892b-be7943b4fdca
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---


# Sharp{#sharp}

Aprimoramento de material padrão. Define o modo padrão de nitidez do material caso um registro de catálogo específico não contenha um valor válido de catalog::Sharp.

## Propriedades {#section-dcb810d01b8a40eb991d555a3cbe48b9}

Enum.

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Sem nitidez. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Nitidez normal (após a transformação). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Nitidez alternativa (antes da transformação). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Mais nitidez (antes e depois da transformação). </p> </td> 
 </tr> 
</table>

## Padrão {#section-613130fca7c04ce7a7734265f27aa1ea}

Herdado de `default::Sharp` se não estiver definido ou se estiver vazio.

## Consulte também {#section-7771824f2822443ab0297e8793bb48ae}

[catálogo::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a),  [catálogo::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
