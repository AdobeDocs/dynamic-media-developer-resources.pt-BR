---
title: qlt
description: Qualidade do Jpeg. Especifica atributos de codificação do JPEG para controlar o nível de compactação. Isso, por sua vez, varia o tamanho do arquivo (quantidade de dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
TQID: 'https://experienceleague.adobe.com/sf3ydtf3lGCG1BfJfc1vW5hXFBawbeWJwXNSJdUEei8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 0%

---

# qlt{#qlt}

Qualidade do Jpeg. Especifica atributos de codificação do JPEG para controlar o nível de compactação. Isso, por sua vez, varia o tamanho do arquivo (quantidade de dados de resposta) e, indiretamente, a qualidade visual da imagem resultante.

` qlt= *`Qualidade`*[, *`croma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> qualidade </span> </span> </p> </td> 
  <td class="stentry"> <p>Qualidade de codificação do JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> </span> </span> </p> </td> 
  <td class="stentry"> <p>Redução da resolução de cromaticidade de JPEG (0=normal, 1=desabilitado); opcional, o padrão é 0. </p> </td> 
 </tr> 
</table>

Usado apenas se `fmt=jpg`. Ignorado caso contrário

Valores de qualidade mais altos aumentam o tamanho e a qualidade do arquivo, valores mais baixos diminuem os tamanhos do arquivo e reduzem a qualidade da imagem percebida. Valores acima de 90 geralmente geram imagens indistinguíveis da imagem descompactada.

Defina o sinalizador `chroma` para desabilitar a redução de resolução de cromaticidade de RGB usada por codificadores JPEG típicos. Isso pode aumentar a nitidez percebida das arestas em uma imagem quando a aresta é definida por uma alteração no matiz em vez do brilho. A definição desse sinalizador pode causar um pequeno aumento no tamanho do arquivo. Experimente essa configuração se o texto parecer ligeiramente indefinido.

O `chroma` será ignorado se o tipo de pixel de saída for CMYK ou cinza.

## Exemplo {#section-a6c263f15c29424a86ef267c96a6630a}

`http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80`
