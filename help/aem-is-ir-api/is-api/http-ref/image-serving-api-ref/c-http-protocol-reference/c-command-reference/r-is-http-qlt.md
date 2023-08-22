---
title: qlt
description: qualidade do JPEG. Especifica atributos de codificação de JPEG para controlar o nível de compactação. Isso, por sua vez, varia o tamanho do arquivo (quantidade de dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# qlt{#qlt}

qualidade do JPEG. Especifica atributos de codificação de JPEG para controlar o nível de compactação. Isso, por sua vez, varia o tamanho do arquivo (quantidade de dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.

` qlt= *`qualidade`*[, *`chroma`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> qualidade </span> </p> </td> 
  <td class="stentry"> <p>qualidade de codificação JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> chroma </span> </p> </td> 
  <td class="stentry"> <p>Redução de resolução de cromaticidade de JPEG (0=normal, 1=desabilitado); opcional, o padrão é 0. </p> </td> 
 </tr> 
</table>

Maior *`quality`* Os valores do aumentam o tamanho e a qualidade do arquivo, os valores mais baixos diminuem os tamanhos dos arquivos e reduzem a qualidade da imagem aparente. Valores acima de 90 geralmente geram imagens indistinguíveis da imagem descompactada.

Defina o *`chroma`* sinalizador para desativar a redução de resolução de cromaticidade de RGB usada por codificadores de JPEG típicos. Isso pode aumentar a nitidez percebida das arestas em uma imagem quando a aresta é definida por uma alteração no matiz em vez do brilho. A definição desse sinalizador pode causar um pequeno aumento no tamanho do arquivo. Experimente essa configuração se o texto parecer ligeiramente indefinido.

## Propriedades {#section-925a44cbdc9042db8d4eb149cd073d21}

Solicitar atributo. Aplica-se independentemente da configuração atual da camada. Ignorado se o formato do arquivo de imagem de saída não suportar codificação JPEG. Consulte a descrição de `fmt=` para obter informações sobre quais formatos de imagem de saída são compatíveis `qlt=`.

*`chroma`* é ignorado se o tipo de pixel de saída for CMYK ou cinza.

## Padrão {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## Exemplo {#section-d7d33871d401433aa51d028823eae7a9}

Reduza a qualidade para uma transmissão mais rápida através de uma conexão de baixa largura de banda:

`http://server/myRoodId/myImageId?qlt=60&wid=300`

Aumente a qualidade para conexões de alta largura de banda:

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## Consulte também {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
