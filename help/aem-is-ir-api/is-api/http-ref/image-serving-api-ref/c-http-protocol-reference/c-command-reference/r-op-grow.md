---
title: op_growth
description: Dilata/erode a imagem. Aplica um dilatador morfológico (raio > 0) ou erosão (raio < 0) aos dados da imagem.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# op_growth{#op-grow}

Dilata/erode a imagem. Aplica um dilatador morfológico (raio > 0) ou erosão (raio &lt; 0) aos dados da imagem.

`op_grow= *`raio`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p> </td> 
  <td class="stentry"> <p>Raio de dilatação/erosão em pixels (int -100..100). </p></td> 
 </tr> 
</table>

`*`radius`*` está em pixels relativos à imagem composta. Se a imagem for colorida, cada componente será processado independentemente.

Usado principalmente para modificar o tamanho dos efeitos de camada. Também é útil para obter efeitos especiais em camadas de texto ou camadas de cores sólidas com máscaras.

## Propriedades {#section-b1c66d65168d4ea695e8662ea690bd4e}

Atributo de camada. Aplica-se à camada atual ou à imagem composta, se `layer=comp`.

## Padrão {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, sem alterações.

## Consulte também {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Efeitos de camada](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
