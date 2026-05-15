---
title: op_growthMask
description: Dilata/erode a imagem. Aplica um dilatador morfológico (raio > 0) ou erosão (raio < 0) aos dados da máscara.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 322d97af-bb1b-44bb-90f1-cda9984b78b5
TQID: 'https://experienceleague.adobe.com/-MDsQlyw5ts3RL59hw4-EeF146qdxZqc3fOfzL8BUOA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
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
