---
title: printRes
description: Resolução de impressão. Substitui o valor de resolução de impressão incorporado na imagem de resposta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# printRes{#printres}

Resolução de impressão. Substitui o valor de resolução de impressão incorporado na imagem de resposta.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Resolução de impressão (dpi). </p></td> 
 </tr> 
</table>

A resolução de impressão é normalmente definida por `catalog::PrintResolution` se for uma entrada de catálogo, caso contrário, pelo valor de resolução de impressão incorporado na imagem de origem. Se houver um modelo ou uma imagem composta em camadas, a resolução de impressão padrão incorporada no arquivo de resposta será a resolução de impressão da imagem da camada com o número de camada mais baixo.

A definição da resolução de impressão não altera o tamanho do pixel da imagem de resposta.

## Propriedades {#section-03c7910ebe234804a319e5d0d8ef3a74}

Solicitar atributo. Ela se aplica independentemente da configuração atual da camada.

## Padrão {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution`
Ou a resolução de impressão incorporada na imagem de origem.

## Consulte também {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catálogo::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
