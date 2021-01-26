---
description: Use essas configurações do servidor para definir os limites de tamanho da imagem.
seo-description: Use essas configurações do servidor para definir os limites de tamanho da imagem.
seo-title: Limites de tamanho de imagem
solution: Experience Manager
title: Limites de tamanho de imagem
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6736e652-c495-45a2-bdd2-9975f99af0a2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# Limites de tamanho de imagem{#image-size-limits}

Use essas configurações do servidor para definir os limites de tamanho da imagem.

## IS::MaxMessageSize - Limite de Tamanho de Resposta {#section-bd942385d4d144cd904003695d72c85e}

Limita o tamanho dos dados que o Servidor de Imagens tem permissão para enviar ao Servidor de Plataformas. Efetivamente, isso limita o tamanho da imagem de resposta codificada/compactada que o Serviço de imagem pode retornar ao cliente via HTTP (Mbytes).

## IS::MaxRenderRgnPixels - Limite de Tamanho de Imagem de Saída {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Limita o tamanho das imagens que o Servidor de imagens pode produzir (exceto imagens salvas no arquivo). Valor inteiro maior que 0 em milhões de pixels. Um erro será retornado se uma operação de renderização exceder o limite de tamanho. O padrão é 16.

## IS::MaxSavePixels - Limite de tamanho para salvar em arquivos {#section-d1547c4afa88467080ab08356f775e06}

Limita o tamanho das imagens que o Servidor de imagens gravará nos arquivos com o comando `req=saveToFile`. Valor inteiro maior que 0 em milhões de pixels. Um erro será retornado se a operação de salvar o arquivo exceder esse limite. O padrão é 100 milhões de pixels.

## IS::MaxNonDsfSize - Limite De Tamanho Para Imagens De Entrada Não PTIFF {#section-50de28a7158a436393cce5da0d1e4d46}

O tamanho máximo (em pixels) de imagens que não são PTIFFs que o Servidor de imagens tem permissão para abrir. O Serviço de imagem retornará um erro quando for feita uma tentativa de acessar uma imagem não PTIFF maior que esse limite.

>[!NOTE]
>
>A configuração desse valor muito alto pode fazer com que o Servidor de imagens fique sem memória e resultar em falhas, incluindo falhas.

