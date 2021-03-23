---
description: Use essas configurações do servidor para definir limites de tamanho de imagem.
seo-description: Use essas configurações do servidor para definir limites de tamanho de imagem.
seo-title: Limites de tamanho de imagem
solution: Experience Manager
title: Limites de tamanho de imagem
uuid: 6736e652-c495-45a2-bdd2-9975f99af0a2
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# Limites de tamanho de imagem{#image-size-limits}

Use essas configurações do servidor para definir limites de tamanho de imagem.

## IS::MaxMessageSize - Limite de Tamanho da Resposta {#section-bd942385d4d144cd904003695d72c85e}

Limita o tamanho dos dados que o Servidor de Imagem pode enviar para o Servidor de Plataforma. Na verdade, isso limita o tamanho da imagem de resposta codificada/compactada que o Image Serving pode retornar ao cliente via HTTP (Mbytes).

## IS::MaxRenderRgnPixels - Limite de Tamanho da Imagem de Saída {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Limita o tamanho das imagens que o Servidor de imagem pode produzir (excluindo imagens salvas no arquivo). Valor inteiro maior que 0 em milhões de pixels. Um erro é retornado se uma operação de renderização exceder o limite de tamanho. O padrão é 16.

## IS::MaxSavePixels - Limite de Tamanho para Salvar em Arquivos {#section-d1547c4afa88467080ab08356f775e06}

Limita o tamanho das imagens que o Servidor de Imagens gravará nos arquivos com o comando `req=saveToFile`. Valor inteiro maior que 0 em milhões de pixels. Um erro é retornado se a operação de salvamento de arquivo exceder esse limite. O padrão é 100 milhões de pixels.

## IS::MaxNonDsfSize - Size Limit For Non-PTIFF Input Images {#section-50de28a7158a436393cce5da0d1e4d46}

O tamanho máximo (em Mpixels) de imagens que não são PTIFFs que o Servidor de Imagem tem permissão para abrir. O Image Serving retornará um erro quando uma tentativa é feita para acessar uma imagem que não é PTIFF e que é maior que esse limite.

>[!NOTE]
>
>Definir esse valor como muito alto pode fazer com que o servidor de imagem fique sem memória e resultar em falhas, incluindo falhas.

