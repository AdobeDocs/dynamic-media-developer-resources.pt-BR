---
description: Qualidade Jpeg. Especifica atributos de codificação JPEG para controlar o nível de compactação.
seo-description: Qualidade Jpeg. Especifica atributos de codificação JPEG para controlar o nível de compactação.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 46f5b0da-7fe7-4daf-947b-bb5f5f5f5e6d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# qlt{#qlt}

Qualidade Jpeg. Especifica atributos de codificação JPEG para controlar o nível de compactação.

` qlt= *``*[. *`qualiticroma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> qualidade  </span> </p> </td> 
  <td class="stentry"> <p>Qualidade de codificação JPEG (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> croma  </span> </p> </td> 
  <td class="stentry"> <p>Redução da amostragem de cromaticidade JPEG (0=normal, 1=desativado); opcional, o padrão é 0. </p> </td> 
 </tr> 
</table>

Especifica atributos de codificação JPEG para controlar o nível de compactação. Isso, por sua vez, varia o tamanho do arquivo (quantidade de dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.

Valores mais altos *`quality`* aumentam o tamanho e a qualidade do arquivo, valores mais baixos diminuem os tamanhos de arquivo e reduzem a qualidade da imagem percebida. Valores acima de 90 geralmente geram imagens indistinguíveis da imagem não compactada.

Defina o sinalizador *`chroma`* para desativar a redução da amostragem de cromaticidade empregada pelos codificadores JPEG típicos. Isso pode aumentar a nitidez perceptível das bordas em uma imagem quando a borda é definida por uma mudança de matiz em vez de brilho. A configuração desse sinalizador pode causar um pequeno aumento no tamanho do arquivo. Experimente essa configuração se o texto parecer ligeiramente indefinido.

## Propriedades {#section-897b61c786dd4230a2c5807f2f40e722}

Pode ocorrer em qualquer lugar na solicitação.

Ignorado se o formato de imagem de saída não oferecer suporte à compactação JPEG. Consulte a descrição de `fmt=` para obter uma lista de formatos de imagem de saída compatíveis com a compactação JPEG.

## Padrão {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Consulte também {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [atributo::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
