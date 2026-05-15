---
description: Dados de destino do zoom. Nenhuma ou mais propriedades de direcionamento de zoom, que podem ser usadas em conjunto com o cliente do visualizador de zoom.
solution: Experience Manager
title: Metas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
TQID: 'https://experienceleague.adobe.com/kP22kltIPZqErqxNKpYp2eNkII-GdYQQeiVH3wEYOvM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 0%

---

# Metas{#targets}

Dados de destino do zoom. Nenhuma ou mais propriedades de direcionamento de zoom, que podem ser usadas em conjunto com o cliente do visualizador de zoom.

O servidor retorna o conteúdo desse campo em resposta a `req=targets`, após substituir os tokens de terminador de registro &#39; `??`&#39;.

Até quatro propriedades podem ser associadas a cada alvo de zoom:

` Target. *`núm`*.frame= *`quadro`*`

` Target. *`núm`*.rect= *`esquerda,superior,largura,altura`*`

` Target. *`núm`*.label= *`rótulo`*`

` Target. *`num`*.userData= *`userData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de destino do zoom (int); os destinos do zoom devem ser numerados sequencialmente e consecutivamente, começando com 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> quadro </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de quadro/página opcional para direcionar um quadro/página específico de uma rotação ou conjunto de folhetos; o padrão é 0, se não estiver especificado para uso do visualizador de folheto e rotação; ignorado pelo visualizador de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> esquerda, </span> </span> superior </p> </td> 
  <td class="stentry"> <p>Deslocamento de pixel do canto superior esquerdo da imagem para o canto superior esquerdo do retângulo de destino de zoom (int, int); deve ser 0 ou maior. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> largura, altura </span> </span> </p> </td> 
  <td class="stentry"> <p>O tamanho do pixel do retângulo de destino do zoom (int, int); deve ser maior que 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rótulo </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor de dados de texto; pode ser usado como rótulo de texto para um link de destino de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor de dados de texto; pode ser usado para passar informações específicas do destino para o cliente, como um valor de SKU ou URL de hot link. </p> </td> 
 </tr> 
</table>

Público alvo. *`num`*.rect é necessário para cada destino de zoom e deve especificar um retângulo totalmente dentro da imagem. Todas as outras propriedades são opcionais.

*`label`* e *`userData`* participam da localização da cadeia de texto. Consulte [Localização de Cadeia de Caracteres de Texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) na *Referência de Protocolo HTTP* para obter detalhes.

Para aplicativos envolvendo os clientes do visualizador de folheto e rotação, os destinos de zoom devem ser definidos no mesmo registro de catálogo que define o conjunto de imagens. Quaisquer definições de destino de zoom nos registros de catálogo dos membros do conjunto de imagens são ignoradas pelo visualizador.

Os visualizadores do Dynamic Media esperam destinos de zoom nas coordenadas da imagem com resolução total já ajustada pelos comandos de `catalog::Modifier`.

## Propriedades {#section-b3f8eba4985f4b00bb935d592fe770f9}

Valor de [dados de propriedade](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md).

## Padrão {#section-feab29f6575e482391086a57f547543c}

Nenhum.

## Consulte também {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catálogo::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catálogo::Modificador](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Localização de Cadeia de Caracteres de Texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
