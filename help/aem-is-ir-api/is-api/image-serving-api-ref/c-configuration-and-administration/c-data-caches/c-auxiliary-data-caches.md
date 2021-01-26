---
description: Os dados de imagem intermediários produzidos pelas solicitações aninhadas/incorporadas do Serviço de imagem e da Renderização de imagem podem ser armazenados em cache especificando cache=on na solicitação aninhada/incorporada. Esses dados são armazenados em formato proprietário no cache de dados de resposta.
seo-description: Os dados de imagem intermediários produzidos pelas solicitações aninhadas/incorporadas do Serviço de imagem e da Renderização de imagem podem ser armazenados em cache especificando cache=on na solicitação aninhada/incorporada. Esses dados são armazenados em formato proprietário no cache de dados de resposta.
seo-title: Caches de dados auxiliares
solution: Experience Manager
title: Caches de dados auxiliares
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# Caches de dados auxiliares{#auxiliary-data-caches}

Os dados de imagem intermediários produzidos pelas solicitações aninhadas/incorporadas do Serviço de imagem e da Renderização de imagem podem ser armazenados em cache especificando cache=on na solicitação aninhada/incorporada. Esses dados são armazenados em formato proprietário no cache de dados de resposta.

As imagens obtidas de servidores HTTP externos também são armazenadas no cache de dados de resposta. Essas imagens são validadas automaticamente com o utilitário de validação antes da entrada do cache ser gerada.

O Servidor de plataforma compila dados do catálogo de imagens para um acesso eficiente. Esses dados são armazenados em `CS::CatalogCacheFolder`.
