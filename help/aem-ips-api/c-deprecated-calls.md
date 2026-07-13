---
title: Chamadas obsoletas
description: Chamadas de API do Sistema de Produção de Imagens e seus parâmetros associados que não são mais usados ou suportados em  [!DNL Dynamic Media].
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
autotag-review: '2026-05-13T21:03:57.183Z'
TQID: 'https://experienceleague.adobe.com/JLoyXksHQ-LAXXxfY71Dv-FOE0trpt-RzcKcV-Pv96I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 0%

---

# Chamadas obsoletas{#deprecated-calls}

Chamadas da API do sistema de produção de imagens e seus parâmetros associados que não são mais usados.

## Chamadas obsoletas {#topic-654c0466e6434fe4a95953322255b08c}

Chamadas de API do Sistema de Produção de Imagens e seus parâmetros associados que não são mais usados em [!DNL Dynamic Media].

* `ExcludeMasterVideoFromAVS` - Obsoleto de [Tipos de dados](/help/aem-ips-api/types/c-data-types/c-data-types.md). Esse parâmetro excluiu o vídeo principal do conjunto de vídeos adaptáveis. <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` - Obsoleto de [Operações](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Esse parâmetro permite adicionar um Evento do Portal de mídia ao IPS.
* `getMediaPortalEvent` - Obsoleto de [Operações](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Esse parâmetro permite obter eventos do portal de mídia que correspondam a critérios especificados.
* `getCdnCacheInvalidationStatus` - Obsoleto de [Operações](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Este parâmetro agora está obsoleto porque o parâmetro `cdnCacheInvalidation` invalida o cache quase imediatamente (~5 segundos). Dessa forma, a pesquisa do status de invalidação não é mais necessária.

