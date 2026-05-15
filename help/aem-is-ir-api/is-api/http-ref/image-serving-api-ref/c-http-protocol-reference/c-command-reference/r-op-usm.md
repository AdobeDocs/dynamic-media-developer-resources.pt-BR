---
title: op_usm
description: Tirar nitidez da máscara. Tirar nitidez mascara a camada ou a imagem de exibição final, após todo o dimensionamento, se layer=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
TQID: 'https://experienceleague.adobe.com/Q2-9E1SNDgr8rGYWNKDLlVcQU85EhpEXhxAqF3WrJic'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 0%

---

# op_usm{#op-usm}

Tirar nitidez da máscara. Tirar nitidez mascara a camada ou a imagem de exibição final, após todo o dimensionamento, se layer=comp.

Pressupõe-se que os parâmetros se aplicam à imagem com resolução total e são reduzidos ao processar uma imagem com resolução reduzida.

`op_usm= *`quantidade`*[, *`raio`*[, *`limite`*[, *`monocromático`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> valor</span></span> </p></td> 
  <td class="stentry"> <p>Fator de resistência do filtro (real 0 a 5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p></td> 
  <td class="stentry"> <p>Filtrar raio do kernel em pixels (real 0 a 250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> limite</span></span> </p></td> 
  <td class="stentry"> <p>Nível limite do filtro (int 0 a 255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monocromático</span></span> </p></td> 
  <td class="stentry"> <p>Defina como 0 para aplicar separadamente cada componente de cor, ou como 1 para aplicar somente ao brilho da imagem (intensidade). </p> <p> <span class="codeph"><span class="varname"> monocromático</span></span> é ignorado para imagens em tons de cinza. </p></td> 
 </tr> 
</table>

A máscara de camada ou a máscara composta também é afiada.

## Propriedades {#section-fb5311b34d164946b74dadb32359518a}

Atributo de camada ou atributo de exibição. Aplica-se à camada atual ou à imagem de exibição final, se `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` para nenhum efeito de máscara sem nitidez.

## Consulte também {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
