---
description: Zoom nos dados do público alvo. Nenhuma ou mais propriedades de público alvo de zoom, que podem ser usadas em conjunto com o cliente do visualizador de zoom.
seo-description: Zoom nos dados do público alvo. Nenhuma ou mais propriedades de público alvo de zoom, que podem ser usadas em conjunto com o cliente do visualizador de zoom.
seo-title: Públicos alvos
solution: Experience Manager
title: Públicos alvos
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ca02483a-9aa0-4b54-b6f0-4fd10d8b2b4c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---


# Públicos alvos{#targets}

Zoom nos dados do público alvo. Nenhuma ou mais propriedades de público alvo de zoom, que podem ser usadas em conjunto com o cliente do visualizador de zoom.

O servidor retorna o conteúdo desse campo em resposta a `req=targets`, depois de substituir os tokens de terminador de registros &#39; `??`&#39;.

Até quatro propriedades podem ser associadas a cada público alvo de zoom:

` Target. *``*.frame= *`número`*`

` Target. *``*.rect= *`número esquerdo,superior,largura,altura`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num  </span> </span> </p> </td> 
  <td class="stentry"> <p>Número do público alvo de zoom (int); públicos alvos de zoom devem ser numerados sequencialmente e consecutivamente, começando com 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> quadro  </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de quadro/página opcional para direcionar um quadro/página específico de um conjunto de giro ou brochura; O padrão é 0 se não for especificado para o uso do visualizador de giro e brochura; ignorado pelo visualizador de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> esquerda, topo  </span> </span> </p> </td> 
  <td class="stentry"> <p>Deslocamento de pixel da parte superior esquerda da imagem para a parte superior esquerda do retângulo do público alvo de zoom (int, int); deve ser 0 ou maior. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> largura, altura  </span> </span> </p> </td> 
  <td class="stentry"> <p>Tamanho em pixels do retângulo do público alvo de zoom (int, int); deve ser maior que 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor dos dados do texto; pode ser usado como um rótulo de texto para um link de público alvo de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor dos dados do texto; pode ser usado para transmitir informações específicas do público alvo ao cliente, como um valor de SKU ou um URL de link ativo. </p> </td> 
 </tr> 
</table>

Público alvo. *`num`*.rect é necessário para cada público alvo de zoom e deve especificar um retângulo totalmente na imagem. Todas as outras propriedades são opcionais.

*`label`* e  *`userData`* participar da localização da string de texto. Consulte [Localização de cadeia de caracteres de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) na *Referência de protocolo HTTP* para obter detalhes.

Para aplicativos que envolvam os clientes do visualizador de giro e folheto, os públicos alvos de zoom devem ser definidos no mesmo registro de catálogo que define o conjunto de imagens. Quaisquer definições de público alvo de zoom nos registros de catálogo dos membros do conjunto de imagens são ignoradas pelo visualizador.

Os visualizadores do Dynamic Media esperam públicos alvos de zoom nas coordenadas da imagem de resolução completa já ajustada pelos comandos de `catalog::Modifier`.

## Propriedades {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Valor ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) dos dados da propriedade.

## Padrão {#section-feab29f6575e482391086a57f547543c}

Nenhum.

## Consulte também {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catálogo::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) ,  [catálogo::Modificador](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834),  [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), Localização de string de  [texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
