---
description: Os dados de imagem intermediários produzidos por solicitações aninhadas/incorporadas de Exibição de imagem e Renderização de imagem podem ser armazenados em cache especificando cache=on na solicitação aninhada/incorporada. Esses dados são armazenados em formato proprietário no cache de dados de resposta.
seo-description: Os dados de imagem intermediários produzidos por solicitações aninhadas/incorporadas de Exibição de imagem e Renderização de imagem podem ser armazenados em cache especificando cache=on na solicitação aninhada/incorporada. Esses dados são armazenados em formato proprietário no cache de dados de resposta.
seo-title: Caches de dados auxiliares
solution: Experience Manager
title: Caches de dados auxiliares
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Caches de dados auxiliares{#auxiliary-data-caches}

Os dados de imagem intermediários produzidos por solicitações aninhadas/incorporadas de Exibição de imagem e Renderização de imagem podem ser armazenados em cache especificando cache=on na solicitação aninhada/incorporada. Esses dados são armazenados em formato proprietário no cache de dados de resposta.

As imagens obtidas de servidores HTTP externos também são armazenadas no cache de dados de resposta. Essas imagens são validadas automaticamente com o utilitário validate antes da entrada do cache ser gerada.

O servidor da plataforma compila dados do catálogo de imagens para obter um acesso eficiente. Esses dados são armazenados em `CS::CatalogCacheFolder`.
