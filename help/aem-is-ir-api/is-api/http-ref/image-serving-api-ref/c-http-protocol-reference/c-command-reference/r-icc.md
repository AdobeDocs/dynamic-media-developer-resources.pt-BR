---
description: Perfil de cor de saída.
seo-description: Perfil de cor de saída.
seo-title: icc
solution: Experience Manager
title: icc
topic: Dynamic Media Image Serving - Image Rendering API
uuid: cfbd18aa-cbba-4085-920d-1f54645d0f89
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---


# icc{#icc}

Perfil de cor de saída.

`icc= *``*[, *``*[, *``*[, *`objectrenderIntentblackpointCompdither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> objeto</span> </span> </p></td> 
  <td class="stentry"> <p>PERFIL de cor ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> perceptual|relativo|saturação|absoluto</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 para ativar, 0 para desativar a compensação do ponto de interrupção. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pontilhado</span></span> </p></td> 
  <td class="stentry"> <p>1 para ativar, 0 para desativar o pontilhamento. </p></td> 
 </tr> 
</table>

*`object`* especifica o perfil de espaço de cor de saída para o qual a imagem deve ser convertida se for diferente do perfil em funcionamento. *`profile`* deve ser um caminho válido  `icc::Name` definido no mapa de perfis ICC de um catálogo de imagens ou catálogo padrão, ou um caminho relativo para um arquivo de perfil (normalmente com  [!DNL .icc] ou  [!DNL .icm] sufixo). Consulte [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)para obter mais informações.

>[!NOTE]
>
>*`object`* não pode incluir caracteres &#39;,&#39;, mesmo se codificados por HTTP.

*`renderIntent`* permite substituir o propósito de renderização padrão.

*`blackpointComp`* ativa a compensação de ponto negrito se o perfil de saída suportar esse recurso.

>[!NOTE]
>
>Nem todas as conversões de cores suportam todas as *`renderIntent`* e *`blackpointComp`* opções. Normalmente, essas configurações são respeitadas somente quando o perfil de saída ICC caracteriza um dispositivo de saída, como uma impressora ou monitor. Além disso, alguns perfis de saída ICC não suportam todas as *`renderIntent`* opções.

Nota

*`dither`* permite o pontilhamento (na verdade, a difusão de erros), que pode evitar ou reduzir artefatos de faixas de cores.

## Propriedades {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Atributo de solicitação. O servidor retornará um erro se um tipo de imagem for especificado com `fmt=` que não corresponde a *`profile`*.

*`renderIntent`* e  *`blackpointComp`* são ignorados se não forem compatíveis com o perfil ICC especificado. PERFIS de dispositivo de saída CMYK têm maior probabilidade de suportar propósitos de renderização diferentes.

## Padrão {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Se o gerenciamento de cores estiver ativado e `icc=` não for especificado, o servidor entregará a imagem convertida no perfil de saída ( `attribute::IccProfile*`) correspondente ao tipo de imagem especificado com `fmt=`.

Se não for especificado, *`renderIntent`* será herdado de `attribute::IccRenderIntent`, *`blackpointComp`* será herdado de `attribute::IccBlackPointCompensation` e *`dither`* será herdado de `attribute::IccDither`.

## Consulte também {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[atributo::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) ,  [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [atributo::IccBlackPointCompensação](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f),  [atributo::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)  [ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)  [object, Gerenciamento de Cores, Referência Map do Perfil ICCEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
