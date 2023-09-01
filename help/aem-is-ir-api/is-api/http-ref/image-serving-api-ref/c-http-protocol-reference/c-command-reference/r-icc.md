---
title: icc
description: Perfil de cores de saída.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# icc{#icc}

Perfil de cores de saída.

`icc= *`objeto`*[, *`renderIntent`*[, *`blackpointComp`*[, *`pontilhamento`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> objeto</span> </span> </p></td> 
  <td class="stentry"> <p>Perfil de cores ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> perceptivo|relativo|saturação|absoluto</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 para ativar, 0 para desativar a compensação de ponto de bloqueio. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pontilhamento</span></span> </p></td> 
  <td class="stentry"> <p>1 para ativar, 0 para desativar o pontilhamento. </p></td> 
 </tr> 
</table>

O valor *`object`* especifica o perfil do espaço de cores de saída no qual a imagem deve ser convertida se for diferente do perfil de trabalho. O valor *`profile`* deve ser um válido `icc::Name` definido no mapa de perfis ICC de um catálogo de imagens ou catálogo padrão, ou um caminho relativo para um arquivo de perfil (normalmente com [!DNL .icc] ou [!DNL .icm] sufixo). Consulte [*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) para obter informações adicionais.

>[!NOTE]
>
>O valor *`object`* não pode incluir caracteres &#39;,&#39;, mesmo se codificado em HTTP.

O valor *`renderIntent`* permite substituir a tentativa de renderização padrão.

O valor *`blackpointComp`* ativa a compensação de blackpoint se o perfil de saída suportar esse recurso.

>[!NOTE]
>
>Nem todas as conversões de cores dão suporte a tudo *`renderIntent`* e *`blackpointComp`* opções. Normalmente, essas configurações são respeitadas apenas quando o perfil de saída ICC caracteriza um dispositivo de saída, como uma impressora ou monitor. Além disso, alguns perfis de saída ICC não suportam todos *`renderIntent`* opções.

Nota

O modificador *`dither`* permite o pontilhamento (difusão de erro), que pode evitar ou reduzir artefatos de banda de cores.

## Propriedades {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Solicitar atributo. O servidor retornará um erro se um tipo de imagem for especificado com `fmt=` que não corresponde a *`profile`*.

Os modificadores *`renderIntent`* e *`blackpointComp`* são ignorados se não forem compatíveis com o perfil ICC especificado. Os perfis de dispositivo de saída CMYK têm mais probabilidade de suportar diferentes intenções de renderização.

## Padrão {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Se o gerenciamento de cores estiver ativado e `icc=` não for especificado, o servidor fornecerá a imagem convertida no perfil de saída ( `attribute::IccProfile*`) correspondente ao tipo de imagem especificado com `fmt=`.

Se não especificado, *`renderIntent`* é herdado de `attribute::IccRenderIntent`, *`blackpointComp`* é herdado de `attribute::IccBlackPointCompensation`, e *`dither`* é herdado de `attribute::IccDither`.

## Consulte também {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Gerenciamento de cores](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7), [Referência do mapa de perfis ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
