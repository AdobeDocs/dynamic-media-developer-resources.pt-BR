---
title: Chamadas obsoletas
description: Chamadas da API do sistema de produção de imagens e seus parâmetros associados que não são mais usados no Dynamic Media.
solution: Experience Manager
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# Chamadas obsoletas{#deprecated-calls}

Chamadas da API do sistema de produção de imagens e seus parâmetros associados que não são mais usados.

## Chamadas obsoletas {#topic-654c0466e6434fe4a95953322255b08c}

Chamadas da API do sistema de produção de imagens e seus parâmetros associados que não são mais usados no Dynamic Media.

* `addMediaPortalEvent` - Obsoleto das operações. Esta chamada permite que você adicione um Evento do Portal de mídia ao IPS.
* `getMediaPortalEvent` - Obsoleto das operações. Esta chamada permite obter eventos de portal de mídia que correspondem a critérios especificados.
* `getCdnCacheInvalidationStatus` - Obsoleto das operações. Essa API agora está obsoleta porque a API `cdnCacheInvalidation` invalida o cache quase imediatamente (~5 segundos). Dessa forma, a pesquisa para o status de invalidação não é mais necessária.

