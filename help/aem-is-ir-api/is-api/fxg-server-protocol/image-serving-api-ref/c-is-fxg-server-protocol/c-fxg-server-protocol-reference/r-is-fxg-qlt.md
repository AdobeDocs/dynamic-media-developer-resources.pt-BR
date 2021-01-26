---
description: Qualidade Jpeg. Especifica atributos de codificação JPEG para controlar o nível de compactação. Isso, por sua vez, varia o tamanho do arquivo (quantidade de dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.
seo-description: Qualidade Jpeg. Especifica atributos de codificação JPEG para controlar o nível de compactação. Isso, por sua vez, varia o tamanho do arquivo (quantidade de dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 936607c1-20c3-4f76-b970-614b21c47dea
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# qlt{#qlt}

Qualidade Jpeg. Especifica atributos de codificação JPEG para controlar o nível de compactação. Isso, por sua vez, varia o tamanho do arquivo (quantidade de dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.

` qlt= *``*[, *`qualiticroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> qualidade  </span> </span> </p> </td> 
  <td class="stentry"> <p>Qualidade de codificação JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> croma  </span> </span> </p> </td> 
  <td class="stentry"> <p>Redução da amostragem de cromaticidade JPEG (0=normal, 1=desativado); opcional, o padrão é 0. </p> </td> 
 </tr> 
</table>

Usado somente se `fmt=jpg`. Ignorado caso contrário

Valores de qualidade mais altos aumentam o tamanho e a qualidade do arquivo, valores mais baixos diminuem os tamanhos de arquivo e reduzem a qualidade da imagem percebida. Valores acima de 90 geralmente geram imagens indistinguíveis da imagem não compactada.

Defina o sinalizador `chroma` para desativar a resolução reduzida de cromaticidade RGB empregada por codificadores JPEG típicos. Isso pode aumentar a nitidez perceptível das bordas em uma imagem quando a borda é definida por uma mudança de matiz em vez de brilho. A configuração desse sinalizador pode causar um pequeno aumento no tamanho do arquivo. Experimente essa configuração se o texto parecer ligeiramente indefinido.

`chroma` é ignorada se o tipo de pixel de saída for CMYK ou cinza.

## Exemplo {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
