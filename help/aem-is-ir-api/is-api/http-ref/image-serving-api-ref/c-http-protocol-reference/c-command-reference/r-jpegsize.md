---
title: jpegSize
description: Tamanho do Jpeg em KiloBytes. Especifica o tamanho máximo da resposta do JPEG em quilobytes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08cecb09-100f-4671-b335-d59c88b0e1ef
TQID: 'https://experienceleague.adobe.com/FXPTcUoMZP-mA-PyuaLqLFqqY9ITLWkjWgezRFUDiHI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 0%

---

# jpegSize{#jpegsize}

Tamanho do Jpeg em KiloBytes. Especifica o tamanho máximo da resposta do JPEG em quilobytes.

`jpegSize= *`tamanho`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> tamanho</span></span> </p> </td> 
  <td class="stentry"> <p>Tamanho em quilobytes. </p></td> 
 </tr> 
</table>

Se estiver definida com um valor positivo e se a resposta do JPEG com a qualidade de JPEG especificada não exceder esse valor, essa imagem será retornada como resposta. Caso contrário, a qualidade do JPEG diminui até produzir uma imagem que se ajuste ao tamanho especificado ou até determinar que não se ajuste. No último caso, a solicitação falha com um erro.

Um valor de 0 significa que a resposta não está restrita por tamanho.

Valores negativos não são permitidos.

## Propriedades {#section-19e544e77d35478b98fe8666f27d6968}

Solicitar atributo. Aplica-se independentemente da configuração atual da camada. Ignorado se o formato da imagem de saída não for JPEG.

## Padrão {#section-198b798ed187453197e0969c641d6fb5}

0

## Exemplo {#section-46bf806fd3ef4875b7726df32b6f834d}

O tamanho da garantia não é muito grande para ser entregue a um dispositivo com memória limitada:

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## Consulte também {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
