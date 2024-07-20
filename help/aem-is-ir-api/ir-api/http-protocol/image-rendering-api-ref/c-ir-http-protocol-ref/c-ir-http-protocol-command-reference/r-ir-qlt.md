---
title: qlt
description: Qualidade do Jpeg. Especifica atributos de codificação de JPEG para controlar o nível de compactação.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# qlt{#qlt}

Qualidade do Jpeg. Especifica atributos de codificação de JPEG para controlar o nível de compactação.

` qlt= *`qualidade`*[. *`croma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> qualidade </span> </p> </td> 
  <td class="stentry"> <p>qualidade de codificação do JPEG (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> croma </span> </p> </td> 
  <td class="stentry"> <p>Redução de resolução de cromaticidade de JPEG (0=normal, 1=desabilitado); opcional, o padrão é 0. </p> </td> 
 </tr> 
</table>

Especifica atributos de codificação de JPEG para controlar o nível de compactação. Por sua vez, isso varia o tamanho do arquivo (quantidade de dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.

Valores *`quality`* mais altos aumentam o tamanho e a qualidade do arquivo, valores mais baixos diminuem os tamanhos dos arquivos e reduzem a qualidade da imagem aparente. Valores acima de 90 geralmente geram imagens indistinguíveis da imagem descompactada.

Defina o sinalizador *`chroma`* para desativar a redução de resolução de cromaticidade empregada por codificadores de JPEG típicos. Essa configuração pode aumentar a nitidez percebida das arestas em uma imagem quando a aresta é definida por uma alteração no matiz em vez do brilho. A definição desse sinalizador pode causar um pequeno aumento no tamanho do arquivo. Experimente essa configuração se o texto parecer ligeiramente indefinido.

## Propriedades {#section-897b61c786dd4230a2c5807f2f40e722}

Pode ocorrer em qualquer lugar na solicitação.

Ignorado se o formato de imagem de saída não suportar compactação JPEG. Consulte a descrição de `fmt=` para obter uma lista de formatos de imagem de saída que oferecem suporte à compactação JPEG.

## Padrão {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Consulte também {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
