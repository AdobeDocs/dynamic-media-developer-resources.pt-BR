---
description: Os dados de imagem intermediários produzidos por solicitações aninhadas/incorporadas de Disponibilização de imagem e Renderização de imagem podem ser armazenados em cache especificando cache=on na solicitação aninhada/incorporada. Esses dados são armazenados em formato proprietário no cache de dados de resposta.
solution: Experience Manager
title: Caches de dados auxiliares
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# Caches de dados auxiliares{#auxiliary-data-caches}

Os dados de imagem intermediários produzidos por solicitações aninhadas/incorporadas de Disponibilização de imagem e Renderização de imagem podem ser armazenados em cache especificando cache=on na solicitação aninhada/incorporada. Esses dados são armazenados em formato proprietário no cache de dados de resposta.

Imagens obtidas de servidores HTTP estrangeiros também são armazenadas no cache de dados de resposta. Essas imagens são validadas automaticamente com o utilitário de validação antes da geração da entrada de cache.

A variável [!DNL Platform Server] O compila os dados do catálogo de imagens para um acesso eficiente. Esses dados são armazenados no `CS::CatalogCacheFolder`.
