---
description: Dilate/erode imagem. Aplica um dilatador morfológico (raio > 0) ou erode (raio < 0) aos dados da máscara.
seo-description: Dilate/erode imagem. Aplica um dilatador morfológico (raio > 0) ou erode (raio < 0) aos dados da máscara.
seo-title: op_growthMaskR
solution: Experience Manager
title: op_growthMaskR
uuid: b81968e7-ebaf-426c-9230-1afcf4b5cf24
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# op_growthMaskR{#op-growmaskr}

Dilate/erode imagem. Aplica um dilatador morfológico (raio > 0) ou erode (raio &lt; 0) aos dados da máscara.

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>Dilate/erode radius em pixels onde <span class="codeph"><span class="varname"> radiusR</span></span> é aplicado como está, independentemente de a máscara ser ou não reduzida (int -100..100). </p></td> 
 </tr> 
</table>

Usada principalmente para aumentar ou diminuir ligeiramente uma máscara para evitar artefatos ao redor da borda da máscara.

## Propriedades {#section-b1c66d65168d4ea695e8662ea690bd4e}

Aplica-se à camada atual ou à camada `0` se `layer=comp`.

## Padrão {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`, sem alterações.

## Consulte também {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Efeitos de camada](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_growth](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growthMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
