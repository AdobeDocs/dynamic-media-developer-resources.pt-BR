---
title: Chamadas obsoletas
description: Chamadas de API do sistema de produção de imagens e seus parâmetros associados que não são mais usados no Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# Chamadas obsoletas{#deprecated-calls}

Chamadas de API do sistema de produção de imagens e seus parâmetros associados que não são mais usados.

## Chamadas obsoletas {#topic-654c0466e6434fe4a95953322255b08c}

Chamadas de API do sistema de produção de imagens e seus parâmetros associados que não são mais usados no Dynamic Media.

* `addMediaPortalEvent` - Obsoleto das operações. Essa chamada permite adicionar um Evento do Media Portal ao IPS.
* `getMediaPortalEvent` - Obsoleto das operações. Essa chamada permite obter eventos do portal de mídia que correspondem a critérios especificados.
* `getCdnCacheInvalidationStatus` - Obsoleto das operações. Essa API agora está obsoleta porque a API `cdnCacheInvalidation` invalida o cache quase imediatamente (~5 segundos). Dessa forma, a pesquisa para o status de invalidação não é mais necessária.
