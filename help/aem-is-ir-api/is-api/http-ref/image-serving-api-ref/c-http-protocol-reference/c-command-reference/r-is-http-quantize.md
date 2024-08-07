---
title: quantizar
description: Quantização de cores. Especifica atributos de quantização de cores para a conversão de saída de GIF.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---

# quantizar{#quantize}

Quantização de cores. Especifica atributos de quantização de cores para a conversão de saída de GIF.

` quantize= *`tipo`*[, *`pontilhamento`*[, *`númCores`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tipo </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>Especifica o tipo de paleta. </p> <p>Defina como <span class="codeph"> adaptável </span> para calcular uma paleta ideal para a imagem. </p> <p>Defina como <span class="codeph"> web </span> ou <span class="codeph"> mac </span> para escolher uma paleta predefinida. </p> <p> <p>Observação: O tipo de palete <span class="codeph"> mac </span> só é compatível com os formatos GIF e PNG8, mas não com os formatos GIF-Alpha e PNG8-Alpha.</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> pontilhamento </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off} </span> </p> <p>Especifica as opções de pontilhamento. </p> <p>Definido como <span class="codeph"> difuso </span> para difusão de erro Floyd- Steinberg </p> <p>Defina como <span class="codeph"> off </span> para desabilitar o pontilhamento.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>Número de cores de saída (2-256) </p> <p>Especifica quantas cores são incluídas na paleta </span> adaptável <span class="codeph">.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
   <td colname="col2"> <p>Uma lista separada por vírgulas de cores de RGB forçadas no formato hex6 </p> <p>Permite especificar as cores a serem incluídas em uma paleta </span> adaptável <span class="codeph">. Se o número de cores especificado for menor que <span class="codeph"> <span class="varname"> numColors </span> </span>, as cores adicionais serão calculadas com base no conteúdo da imagem.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-8ab5035055b24b858270d260912a7f3d}

Solicitar atributo. Ela se aplica independentemente da configuração atual da camada. Usado apenas se `fmt=gif`, `fmt=gif-alpha`, `fmt=png8` ou `fmt=png8-alpha`. Ignorado de outra forma.

As cores especificadas com *`colorList`* devem consistir em valores de RGB no formato hex6 (consulte [cor](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) sem o prefixo `0x`. Nenhum outro especificador de cor é permitido. O modificador *`numColors`* deve ser 2-256.

## Padrão {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Exemplo {#section-e34aca7587d548a7ae9d4266b80c9451}

Gere uma miniatura de GIF usando a paleta `web` e sem pontilhamento:

`http:// *`*Servidor*`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Converta a imagem em um GIF bi-tonal com transparência de cor-chave. E, forçar cores para preto e branco:

`http:// *`*Servidor*`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Consulte também {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
