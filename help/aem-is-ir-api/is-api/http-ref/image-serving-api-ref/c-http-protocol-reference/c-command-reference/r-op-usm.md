---
description: Tirar nitidez da máscara. Tirar nitidez mascara a camada ou a imagem de exibição final, após toda a escala, se layer=comp.
solution: Experience Manager
title: op_usm
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# op_usm{#op-usm}

Tirar nitidez da máscara. Tirar nitidez mascara a camada ou a imagem de exibição final, após toda a escala, se layer=comp.

Pressupõe-se que os parâmetros sejam aplicados à imagem de resolução completa e que sejam reduzidos ao processar uma imagem com resolução reduzida.

`op_usm= *``*[, *``*[, *``*[, *`amount tradusthreshold monchrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> quantia</span></span> </p></td> 
  <td class="stentry"> <p>Fator de força do filtro (real 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p></td> 
  <td class="stentry"> <p>Filtrar raio do kernel em pixels (real 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> limite</span></span> </p></td> 
  <td class="stentry"> <p>Nível de limite do filtro (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monocromático</span></span> </p></td> 
  <td class="stentry"> <p>Defina como 0 para aplicar a cada componente de cor separadamente ou como 1 para aplicar somente ao brilho da imagem (intensidade). </p> <p> <span class="codeph"><span class="varname"> </span></span> monocromáticos ignorados para imagens em tons de cinza. </p></td> 
 </tr> 
</table>

A máscara de camada ou máscara composta também é afiada.

## Propriedades {#section-fb5311b34d164946b74dadb32359518a}

Atributo de camada ou atributo de exibição. Aplica-se à camada atual ou à imagem de exibição final se `layer=comp`. Ignorado por camadas de efeito.

## Padrão {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` para nenhum efeito de mascaramento nítido.

## Consulte também {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
