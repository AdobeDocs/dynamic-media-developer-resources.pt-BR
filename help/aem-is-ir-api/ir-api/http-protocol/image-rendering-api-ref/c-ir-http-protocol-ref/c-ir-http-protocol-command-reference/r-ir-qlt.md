---
description: Qualidade Jpeg. Especifica atributos de codificação JPEG para controlar o nível de compactação.
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# qlt{#qlt}

Qualidade Jpeg. Especifica atributos de codificação JPEG para controlar o nível de compactação.

` qlt= *``*[. *`Qualicroma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> qualidade  </span> </p> </td> 
  <td class="stentry"> <p>Qualidade de codificação JPEG (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> croma  </span> </p> </td> 
  <td class="stentry"> <p>Amostragem regressiva da cromaticidade JPEG (0=normal, 1=desativado); opcional, o padrão é 0. </p> </td> 
 </tr> 
</table>

Especifica atributos de codificação JPEG para controlar o nível de compactação. Por sua vez, isso varia o tamanho do arquivo (quantidade dos dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.

Valores mais altos *`quality`* aumentam o tamanho e a qualidade do arquivo, valores mais baixos diminuem os tamanhos dos arquivos e reduzem a qualidade da imagem percebida. Valores acima de 90 geralmente geram imagens indistinguíveis da imagem descompactada.

Defina o sinalizador *`chroma`* para desativar a amostragem regressiva de cromaticidade empregada por codificadores JPEG típicos. Isso pode aumentar a nitidez perceptível das bordas em uma imagem, quando a borda é definida por uma mudança de matiz em vez de brilho. Configurar esse sinalizador pode causar um pequeno aumento no tamanho do arquivo. Experimente essa configuração se o texto parecer ligeiramente borrado.

## Propriedades {#section-897b61c786dd4230a2c5807f2f40e722}

Pode ocorrer em qualquer lugar na solicitação.

Ignorado se o formato de imagem de saída não oferecer suporte à compactação JPEG. Consulte a descrição de `fmt=` para obter uma lista de formatos de imagem de saída que oferecem suporte à compactação JPEG.

## Padrão {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Consulte também {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [atributo::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
