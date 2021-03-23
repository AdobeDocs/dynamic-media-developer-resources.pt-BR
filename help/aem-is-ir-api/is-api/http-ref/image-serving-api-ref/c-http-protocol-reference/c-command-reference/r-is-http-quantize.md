---
description: Quantificação de cores. Especifica atributos de quantificação de cores para conversão de saída GIF.
seo-description: Quantificação de cores. Especifica atributos de quantificação de cores para conversão de saída GIF.
seo-title: quantizar
solution: Experience Manager
title: quantizar
uuid: 4e9c4807-59bc-4eb9-bcab-0bf0cfdf56d4
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# quantizar{#quantize}

Quantificação de cores. Especifica atributos de quantificação de cores para conversão de saída GIF.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac}  </span> </p> <p>Especifica o tipo de paleta. </p> <p>Defina como <span class="codeph"> adaptável </span> para calcular uma paleta ideal para a imagem. </p> <p>Defina como <span class="codeph"> web </span> ou <span class="codeph"> mac </span> para escolher uma paleta predefinida. </p> <p> <p>Observação:  O tipo de palete <span class="codeph"> mac </span> só é suportado para formatos GIF e PNG8, mas não para formatos GIF-Alpha e PNG8-Alpha. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tonalidade  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off}  </span> </p> <p>Especifica as opções de pontilhamento. </p> <p>Defina como <span class="codeph"> difuso </span> para a difusão de erros Floyd-Steinberg </p> <p>Defina para <span class="codeph"> desligado </span> para desativar a ligação à ranhura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
   <td colname="col2"> <p>Número de cores de saída (2-256) </p> <p>Especifica quantas cores estão incluídas na paleta <span class="codeph"> adaptável </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
   <td colname="col2"> <p>Uma lista separada por vírgulas de cores RGB forçadas no formato hex6 </p> <p>Permite que você especifique as cores a serem incluídas em uma paleta <span class="codeph"> adaptável </span>. Se o número de cores especificado for menor que <span class="codeph"> <span class="varname"> numColors </span> </span>, as cores adicionais serão calculadas com base no conteúdo da imagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-8ab5035055b24b858270d260912a7f3d}

Atributo da solicitação. Aplica-se independentemente da configuração de camada atual. Usado somente se `fmt=gif`, `fmt=gif-alpha`, `fmt=png8` ou `fmt=png8-alpha`. Caso contrário, ignorado.

As cores especificadas com `*`colorList`*` devem consistir em valores RGB no formato hexadecimal (consulte ` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`) sem o prefixo &#39; `0x`&#39;. Não são permitidos outros especificadores de cores. *`numColors`* deve estar entre 2 e 256.

## Padrão {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Exemplo {#section-e34aca7587d548a7ae9d4266b80c9451}

Gere uma miniatura GIF usando a paleta `web` e sem pontilhamento:

` http:// *`server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Converta a imagem em um GIF bi-tonal com transparência de cores chave e force as cores para preto e branco:

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Consulte também {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [cor](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
