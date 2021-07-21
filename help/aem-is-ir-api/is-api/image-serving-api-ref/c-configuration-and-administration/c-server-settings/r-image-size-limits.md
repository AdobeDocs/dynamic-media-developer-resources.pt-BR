---
description: Use essas configurações do servidor para definir limites de tamanho de imagem.
solution: Experience Manager
title: Limites de tamanho de imagem
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# Limites de tamanho de imagem{#image-size-limits}

Use essas configurações do servidor para definir limites de tamanho de imagem.

## IS::MaxMessageSize - Limite de Tamanho da Resposta {#section-bd942385d4d144cd904003695d72c85e}

Limita o tamanho dos dados que o Servidor de Imagem pode enviar para o Servidor de Plataforma. Na verdade, isso limita o tamanho da imagem de resposta codificada/compactada que o Image Serving pode retornar ao cliente via HTTP (Mbytes).

## IS::MaxRenderRgnPixels - Limite de Tamanho da Imagem de Saída {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Limita o tamanho das imagens que o Servidor de imagem pode produzir (excluindo imagens salvas no arquivo). Valor inteiro maior que 0 em milhões de pixels. Um erro é retornado se uma operação de renderização exceder o limite de tamanho. O padrão é 16.

## IS::MaxSavePixels - Limite de tamanho para salvar em arquivos {#section-d1547c4afa88467080ab08356f775e06}

Limita o tamanho das imagens que o Servidor de Imagens gravará nos arquivos com o comando `req=saveToFile`. Valor inteiro maior que 0 em milhões de pixels. Um erro é retornado se a operação de salvamento de arquivo exceder esse limite. O padrão é 100 milhões de pixels.

## IS::MaxNonDsfSize - Size Limit For Non-PTIFF Input Images {#section-50de28a7158a436393cce5da0d1e4d46}

O tamanho máximo (em Mpixels) de imagens que não são PTIFFs que o Servidor de Imagem tem permissão para abrir. O Image Serving retornará um erro quando uma tentativa é feita para acessar uma imagem que não é PTIFF e que é maior que esse limite.

>[!NOTE]
>
>Definir esse valor como muito alto pode fazer com que o servidor de imagem fique sem memória e resultar em falhas, incluindo falhas.
