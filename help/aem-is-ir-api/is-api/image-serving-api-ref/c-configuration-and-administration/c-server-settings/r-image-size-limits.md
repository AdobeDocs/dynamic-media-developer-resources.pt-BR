---
description: Use essas configurações do servidor para definir limites de tamanho de imagem.
solution: Experience Manager
title: Limites de tamanho da imagem
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# Limites de tamanho da imagem{#image-size-limits}

Use essas configurações do servidor para definir limites de tamanho de imagem.

## IS::MaxMessageSize - Limite de Tamanho de Resposta {#section-bd942385d4d144cd904003695d72c85e}

Limita o tamanho dos dados que o Servidor de imagens tem permissão para enviar ao [!DNL Platform Server]. Efetivamente, isso limita o tamanho da imagem de resposta codificada/compactada que o Servidor de imagens pode retornar ao cliente por meio de HTTP (Mbytes).

## IS::MaxRenderRgnPixels - Limite de Tamanho da Imagem de Saída {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Limita o tamanho das imagens que o Servidor de imagens pode produzir (excluindo imagens salvas em arquivo). Valor inteiro maior que 0 em milhões de pixels. Um erro é retornado se uma operação de renderização exceder o limite de tamanho. O padrão é 16.

## IS::MaxSavePixels - Limite de tamanho para salvar em arquivos {#section-d1547c4afa88467080ab08356f775e06}

Limita o tamanho das imagens que o Servidor de Imagens grava em arquivos com o comando `req=saveToFile`. Valor inteiro maior que 0 em milhões de pixels. Um erro é retornado se a operação de salvamento de arquivo exceder esse limite. O padrão é 100 milhões de pixels.

## IS::MaxNonDsfSize - Limite de tamanho para imagens de entrada não PTIFF {#section-50de28a7158a436393cce5da0d1e4d46}

O tamanho máximo (em Mpixels) das imagens que não são PTIFFs que o Servidor de imagens tem permissão para abrir. O Servidor de imagens retorna um erro quando é feita uma tentativa de acessar uma imagem não PTIFF maior que esse limite.

>[!NOTE]
>
>Configurar esse valor como alto demais pode fazer com que o Servidor de imagens fique sem memória e resultar em falhas, incluindo falhas.
