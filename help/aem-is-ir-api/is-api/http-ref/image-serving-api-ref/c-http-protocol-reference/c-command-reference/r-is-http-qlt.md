---
title: qlt
description: Qualidade do JPEG. Especifica atributos de codificação do JPEG para controlar o nível de compactação. Isso, por sua vez, varia o tamanho do arquivo (quantidade de dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
TQID: 'https://experienceleague.adobe.com/e7zzYHSi7X5tdPAy-0CWTK-Wqs5nfhEDLs2HYJ1D-f4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 242
ht-degree: 0%

---

# qlt{#qlt}

Qualidade do JPEG. Especifica atributos de codificação do JPEG para controlar o nível de compactação. Isso, por sua vez, varia o tamanho do arquivo (quantidade de dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.

` qlt= *`qualidade`*[, *`croma`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> qualidade </span> </p> </td> 
  <td class="stentry"> <p>Qualidade de codificação do JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> croma </span> </p> </td> 
  <td class="stentry"> <p>Redução da resolução de cromaticidade de JPEG (0=normal, 1=desabilitado); opcional, o padrão é 0. </p> </td> 
 </tr> 
</table>

Valores *`quality`* mais altos aumentam o tamanho e a qualidade do arquivo, valores mais baixos diminuem os tamanhos dos arquivos e reduzem a qualidade da imagem aparente. Valores acima de 90 geralmente geram imagens indistinguíveis da imagem descompactada.

Defina o sinalizador *`chroma`* para desabilitar a redução de resolução de cromaticidade de RGB usada por codificadores JPEG típicos. Isso pode aumentar a nitidez percebida das arestas em uma imagem quando a aresta é definida por uma alteração no matiz em vez do brilho. A definição desse sinalizador pode causar um pequeno aumento no tamanho do arquivo. Experimente essa configuração se o texto parecer ligeiramente indefinido.

## Propriedades {#section-925a44cbdc9042db8d4eb149cd073d21}

Solicitar atributo. Aplica-se independentemente da configuração atual da camada. Ignorado se o formato do arquivo de imagem de saída não suportar codificação JPEG. Consulte a descrição de `fmt=` para obter informações sobre quais formatos de imagem de saída oferecem suporte a `qlt=`.

*`chroma`* será ignorado se o tipo de pixel de saída for CMYK ou cinza.

## Padrão {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## Exemplo {#section-d7d33871d401433aa51d028823eae7a9}

Reduza a qualidade para uma transmissão mais rápida através de uma conexão de baixa largura de banda:

`http://server/myRoodId/myImageId?qlt=60&wid=300`

Aumente a qualidade para conexões de alta largura de banda:

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## Consulte também {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
