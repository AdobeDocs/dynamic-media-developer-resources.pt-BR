---
description: Tamanho Jpeg em KiloBytes. Especifica o tamanho máximo da resposta JPEG em kilobytes.
seo-description: Tamanho Jpeg em KiloBytes. Especifica o tamanho máximo da resposta JPEG em kilobytes.
seo-title: jpegSize
solution: Experience Manager
title: jpegSize
uuid: 832163ca-0554-481d-b87f-bf322f415274
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# jpegSize{#jpegsize}

Tamanho Jpeg em KiloBytes. Especifica o tamanho máximo da resposta JPEG em kilobytes.

`jpegSize= *`size`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> size</span></span> </p> </td> 
  <td class="stentry"> <p>Tamanho em kilobytes. </p></td> 
 </tr> 
</table>

Se isso for definido como um valor positivo e se a resposta JPEG com a qualidade JPEG especificada não exceder esse valor, essa imagem será retornada como resposta. Caso contrário, a qualidade do JPEG diminui até que ele produza uma imagem que se ajuste ao tamanho especificado ou até que determine que não é possível ajustar. No último caso, a solicitação falha com um erro.

Um valor de 0 significa que a resposta não está restrita por tamanho.

Valores negativos não são permitidos.

## Propriedades {#section-19e544e77d35478b98fe8666f27d6968}

Atributo da solicitação. Aplica-se independentemente da configuração de camada atual. Ignorado se o formato de imagem de saída não for JPEG.

## Padrão {#section-198b798ed187453197e0969c641d6fb5}

0

## Exemplo {#section-46bf806fd3ef4875b7726df32b6f834d}

O tamanho da garantia não é muito grande para ser fornecido a um dispositivo com memória limitada:

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## Consulte também {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [atributo::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
