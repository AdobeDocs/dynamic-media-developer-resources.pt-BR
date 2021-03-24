---
description: Qualidade Jpeg. Especifica atributos de codificação JPEG para controlar o nível de compactação. Por sua vez, isso varia o tamanho do arquivo (quantidade dos dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---


# qlt{#qlt}

Qualidade Jpeg. Especifica atributos de codificação JPEG para controlar o nível de compactação. Por sua vez, isso varia o tamanho do arquivo (quantidade dos dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.

` qlt= *``*[, *`Qualicroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> qualidade  </span> </span> </p> </td> 
  <td class="stentry"> <p>Qualidade de codificação JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> croma  </span> </span> </p> </td> 
  <td class="stentry"> <p>Amostragem regressiva da cromaticidade JPEG (0=normal, 1=desativado); opcional, o padrão é 0. </p> </td> 
 </tr> 
</table>

Usado somente se `fmt=jpg`. Ignorado do contrário

Valores de qualidade mais alta aumentam o tamanho e a qualidade do arquivo, valores mais baixos diminuem os tamanhos dos arquivos e reduzem a qualidade da imagem percebida. Valores acima de 90 geralmente geram imagens indistinguíveis da imagem descompactada.

Defina o sinalizador `chroma` para desativar a amostragem suspensa de cromaticidade RGB usada por codificadores JPEG típicos. Isso pode aumentar a nitidez perceptível das bordas em uma imagem, quando a borda é definida por uma mudança de matiz em vez de brilho. Configurar esse sinalizador pode causar um pequeno aumento no tamanho do arquivo. Experimente essa configuração se o texto parecer ligeiramente borrado.

`chroma` é ignorado se o tipo de pixel de saída for CMYK ou cinza.

## Exemplo {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
