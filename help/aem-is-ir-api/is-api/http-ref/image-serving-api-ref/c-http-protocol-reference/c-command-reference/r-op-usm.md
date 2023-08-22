---
title: op_usm
description: Tirar nitidez da máscara. Tirar nitidez mascara a camada ou a imagem de exibição final, após todo o dimensionamento, se layer=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# op_usm{#op-usm}

Tirar nitidez da máscara. Tirar nitidez mascara a camada ou a imagem de exibição final, após todo o dimensionamento, se layer=comp.

Pressupõe-se que os parâmetros se aplicam à imagem com resolução total e são reduzidos ao processar uma imagem com resolução reduzida.

`op_usm= *`quantidade`*[, *`raio`*[, *`limite`*[, *`monocromático`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> quantidade</span></span> </p></td> 
  <td class="stentry"> <p>Fator de resistência do filtro (real 0 a 5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> raio</span></span> </p></td> 
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

Atributo de camada ou atributo de exibição. Aplica-se à camada atual ou à imagem de exibição final se `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` para nenhum efeito de mascaramento sem nitidez.

## Consulte também {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
