---
description: Máscara de nitidez. Tirar nitidez mascara a camada ou a imagem de visualização final, depois de toda a escala, se layer=comp.
seo-description: Máscara de nitidez. Tirar nitidez mascara a camada ou a imagem de visualização final, depois de toda a escala, se layer=comp.
seo-title: op_usm
solution: Experience Manager
title: op_usm
topic: Scene7 Image Serving - Image Rendering API
uuid: c647e063-2405-489b-b14d-a70638ac8af7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_usm{#op-usm}

Máscara de nitidez. Tirar nitidez mascara a camada ou a imagem de visualização final, depois de toda a escala, se layer=comp.

Pressupõe-se que os parâmetros se apliquem à imagem de resolução completa e que sejam reduzidos ao processar uma imagem com resolução reduzida.

`op_usm= *`monocromático`*[, *``*[, *``*[, *`de quantidade`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> quantia</span></span> </p></td> 
  <td class="stentry"> <p>Fator de força do filtro (real 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> raio</span></span> </p></td> 
  <td class="stentry"> <p>Filtrar o raio do kernel em pixels (real 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> limite</span></span> </p></td> 
  <td class="stentry"> <p>Nível limite do filtro (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monocromático</span></span> </p></td> 
  <td class="stentry"> <p>Defina como 0 para aplicar a cada componente colorido separadamente ou como 1 para aplicar somente ao brilho da imagem (intensidade). </p> <p> <span class="codeph"><span class="varname"> O monocromático</span></span> é ignorado para imagens em tons de cinza. </p></td> 
 </tr> 
</table>

A máscara de camada ou a máscara composta também são afiadas.

## Propriedades {#section-fb5311b34d164946b74dadb32359518a}

Atributo de camada ou atributo de visualização. Aplica-se à camada atual ou à imagem de visualização final, se `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` para nenhum efeito de máscara nítida.

## Consulte também {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
