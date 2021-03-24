---
description: Qualidade JPEG. Especifica atributos de codificação JPEG para controlar o nível de compactação. Por sua vez, isso varia o tamanho do arquivo (quantidade dos dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# qlt{#qlt}

Qualidade JPEG. Especifica atributos de codificação JPEG para controlar o nível de compactação. Por sua vez, isso varia o tamanho do arquivo (quantidade dos dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.

` qlt= *``*[, *`Qualicroma`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> qualidade  </span> </p> </td> 
  <td class="stentry"> <p>Qualidade de codificação JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> croma  </span> </p> </td> 
  <td class="stentry"> <p>Amostragem regressiva da cromaticidade JPEG (0=normal, 1=desativado); opcional, o padrão é 0. </p> </td> 
 </tr> 
</table>

Valores mais altos *`quality`* aumentam o tamanho e a qualidade do arquivo, valores mais baixos diminuem os tamanhos dos arquivos e reduzem a qualidade da imagem percebida. Valores acima de 90 geralmente geram imagens indistinguíveis da imagem descompactada.

Defina o sinalizador *`chroma`* para desativar a amostragem suspensa de cromaticidade RGB usada por codificadores JPEG típicos. Isso pode aumentar a nitidez perceptível das bordas em uma imagem, quando a borda é definida por uma mudança de matiz em vez de brilho. Configurar esse sinalizador pode causar um pequeno aumento no tamanho do arquivo. Experimente essa configuração se o texto parecer ligeiramente borrado.

## Propriedades {#section-925a44cbdc9042db8d4eb149cd073d21}

Atributo da solicitação. Aplica-se independentemente da configuração de camada atual. Ignorado se o formato do arquivo de imagem de saída não oferecer suporte à codificação JPEG. Consulte a descrição de `fmt=` para obter informações sobre quais formatos de imagem de saída oferecem suporte para `qlt=`.

*`chroma`* é ignorado se o tipo de pixel de saída for CMYK ou cinza.

## Padrão {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## Exemplo {#section-d7d33871d401433aa51d028823eae7a9}

Reduza a qualidade para transmissão mais rápida através de uma conexão de largura de banda baixa:

`http://server/myRoodId/myImageId?qlt=60&wid=300`

Aumente a qualidade das conexões de alta largura de banda:

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## Consulte também {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [atributo::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
