---
description: Dilate/erode imagem. Aplica um dilatador morfológico (raio > 0) ou erode (raio < 0) aos dados da máscara.
seo-description: Dilate/erode imagem. Aplica um dilatador morfológico (raio > 0) ou erode (raio < 0) aos dados da máscara.
seo-title: op_growthMask
solution: Experience Manager
title: op_growthMask
uuid: 016501e8-33c5-4c9e-8d26-120b1e929c55
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# op_growthMask{#op-growmask}

Dilate/erode imagem. Aplica um dilatador morfológico (raio > 0) ou erode (raio &lt; 0) aos dados da máscara.

`op_growMask= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>Raio de dilato/erode em pixels onde o raio é presumido para aplicar à máscara de resolução completa e, portanto, é dimensionado para menos máscaras (int -100..100). </p></td> 
 </tr> 
</table>

Usada principalmente para aumentar ou diminuir ligeiramente uma máscara para evitar artefatos ao redor da borda da máscara.

## Propriedades {#section-b1c66d65168d4ea695e8662ea690bd4e}

Aplica-se à camada atual ou à camada `0` se `layer=comp`.

## Padrão {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`, sem alterações.

## Consulte também {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Efeitos de camada](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_growth](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growthMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
