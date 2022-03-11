---
title: Chamadas obsoletas
description: Chamadas de API do sistema de produção de imagens e seus parâmetros associados que não são mais usados ou suportados no Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 10eb6887663fe335be3abcc311b2d3eb4a241745
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# Chamadas obsoletas{#deprecated-calls}

Chamadas de API do sistema de produção de imagens e seus parâmetros associados que não são mais usados.

## Chamadas obsoletas {#topic-654c0466e6434fe4a95953322255b08c}

Chamadas de API do sistema de produção de imagens e seus parâmetros associados que não são mais usados no Dynamic Media.

* `ExcludeMasterVideoFromAVS` - Obsoleto de [Tipos de dados](/help/aem-ips-api/types/c-data-types/c-data-types.md). Esse parâmetro excluiu o vídeo principal do conjunto de vídeos adaptáveis.
   >[!IMPORTANT]
   >
   >O Adobe encerrou o suporte a esse parâmetro em 1º de setembro de 2022. Consulte também [ExcludeMasterVideoFromAVS](/help/aem-ips-api/types/c-data-types/r-exclude-master-video-from-avs.md).
* `addMediaPortalEvent` - Obsoleto de [Operações](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Esse parâmetro permite adicionar um Evento do Media Portal ao IPS.
* `getMediaPortalEvent` - Obsoleto de [Operações](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Esse parâmetro permite obter eventos de portal de mídia que correspondem a critérios especificados.
* `getCdnCacheInvalidationStatus` - Obsoleto de [Operações](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Esse parâmetro agora está obsoleto porque a variável `cdnCacheInvalidation` O parâmetro invalida o cache quase imediatamente (~5 segundos). Dessa forma, a pesquisa para o status de invalidação não é mais necessária.
