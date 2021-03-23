---
description: Ampliação dos dados do target. Nenhuma ou mais propriedades de destino de zoom, que podem ser usadas junto com o cliente do visualizador de zoom.
seo-description: Ampliação dos dados do target. Nenhuma ou mais propriedades de destino de zoom, que podem ser usadas junto com o cliente do visualizador de zoom.
seo-title: Metas
solution: Experience Manager
title: Metas
uuid: ca02483a-9aa0-4b54-b6f0-4fd10d8b2b4c
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---


# Metas{#targets}

Ampliação dos dados do target. Nenhuma ou mais propriedades de destino de zoom, que podem ser usadas junto com o cliente do visualizador de zoom.

O servidor retorna o conteúdo desse campo em resposta a `req=targets`, após substituir &#39; `??`&#39; tokens de terminador de registro.

Até quatro propriedades podem ser associadas a cada direcionamento de zoom:

` Target. *``*.frame= *`numframe`*`

` Target. *``*.rect= *`numleft,top,width,height`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num  </span> </span> </p> </td> 
  <td class="stentry"> <p>Número do alvo do zoom (int); os destinos de zoom devem ser numerados sequencialmente e consecutivamente, começando com 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> quadro  </span> </span> </p> </td> 
  <td class="stentry"> <p>Quadro/número de página opcional para direcionar um quadro/página específico de um conjunto de rotação ou brochura; O padrão é 0 se não for especificado para o uso do visualizador de rotação e brochura; ignorado pelo visualizador de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> esquerda, início  </span> </span> </p> </td> 
  <td class="stentry"> <p>Deslocamento de pixels da parte superior esquerda da imagem até a parte superior esquerda do retângulo de destino de zoom (int, int); deve ser 0 ou maior. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> largura, altura  </span> </span> </p> </td> 
  <td class="stentry"> <p>Pixel do retângulo de destino do zoom (int, int); deve ser maior que 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor dos dados do texto; pode ser usado como um rótulo de texto para um link de destino de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor dos dados do texto; pode ser usada para transmitir informações específicas do target ao cliente, como um valor de SKU ou URL de link ativo. </p> </td> 
 </tr> 
</table>

Target. *`num`*.rect é necessário para cada destino de zoom e deve especificar um retângulo totalmente dentro da imagem. Todas as outras propriedades são opcionais.

*`label`* e  *`userData`* participar da localização da string de texto. Consulte [Localização da cadeia de caracteres de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) no *Referência do protocolo HTTP* para obter detalhes.

Para aplicativos que envolvam os clientes do visualizador de rotação e panfleto, os destinos de zoom devem ser definidos no mesmo registro de catálogo que define o conjunto de imagens. Quaisquer definições de direcionamento de zoom nos registros do catálogo dos membros do conjunto de imagens são ignoradas pelo visualizador.

Os visualizadores do Dynamic Media esperam destinos de zoom nas coordenadas da imagem de resolução completa já ajustada pelos comandos de `catalog::Modifier`.

## Propriedades {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Valor dos ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) dados da propriedade.

## Padrão {#section-feab29f6575e482391086a57f547543c}

Nenhum.

## Consulte também {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catálogo::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) ,  [catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834),  [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), Localização da sequência de  [texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
