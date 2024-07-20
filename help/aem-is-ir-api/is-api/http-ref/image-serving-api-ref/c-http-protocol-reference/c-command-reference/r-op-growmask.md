---
title: op_growthMask
description: Dilata/erode a imagem. Aplica um dilatador morfológico (raio > 0) ou erosão (raio < 0) aos dados da máscara.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 322d97af-bb1b-44bb-90f1-cda9984b78b5
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# op_growthMask{#op-growmask}

Dilata/erode a imagem. Aplica um dilatador morfológico (raio > 0) ou erosão (raio &lt; 0) aos dados da máscara.

`op_growMask= *`raio`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>Raio de dilatação/erosão em pixels, onde o raio é aplicado à máscara de resolução total e, portanto, é reduzido para máscaras com resolução reduzida (int -100..100). </p></td> 
 </tr> 
</table>

Usado principalmente para aumentar ou diminuir ligeiramente uma máscara para evitar artefatos ao redor da borda da máscara.

## Propriedades {#section-b1c66d65168d4ea695e8662ea690bd4e}

Aplica-se à camada atual ou à camada `0`, se `layer=comp`.

## Padrão {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`, sem alterações.

## Consulte também {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Efeitos de camada](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_growth](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growthMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
