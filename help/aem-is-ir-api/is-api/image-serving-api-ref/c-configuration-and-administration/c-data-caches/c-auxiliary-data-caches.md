---
description: Os dados de imagem intermediários produzidos por solicitações aninhadas/incorporadas de Exibição de imagem e Renderização de imagem podem ser armazenados em cache especificando cache=on na solicitação aninhada/incorporada. Esses dados são armazenados em formato proprietário no cache de dados de resposta.
solution: Experience Manager
title: Caches de dados auxiliares
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Caches de dados auxiliares{#auxiliary-data-caches}

Os dados de imagem intermediários produzidos por solicitações aninhadas/incorporadas de Exibição de imagem e Renderização de imagem podem ser armazenados em cache especificando cache=on na solicitação aninhada/incorporada. Esses dados são armazenados em formato proprietário no cache de dados de resposta.

As imagens obtidas de servidores HTTP externos também são armazenadas no cache de dados de resposta. Essas imagens são validadas automaticamente com o utilitário validate antes da entrada do cache ser gerada.

O servidor da plataforma compila dados do catálogo de imagens para obter um acesso eficiente. Esses dados são armazenados em `CS::CatalogCacheFolder`.
