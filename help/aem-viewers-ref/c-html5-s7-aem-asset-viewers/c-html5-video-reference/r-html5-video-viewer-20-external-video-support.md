---
title: Suporte a vídeo externo
description: O visualizador suporta a reprodução de vídeo hospedado fora do Dynamic Media Classic ou do Adobe Experience Manager - Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# Suporte a vídeo externo{#external-video-support}

O visualizador suporta a reprodução de vídeo hospedado fora do Dynamic Media Classic ou do Adobe Experience Manager - Dynamic Media.

Os formatos suportados para o vídeo externo são MP4 no formato H.264 ou manifesto M3U8 para fluxo HLS.

O visualizador pode trabalhar com vídeo Dynamic Media Classic ou Experience Manager - Dynamic Media ou com vídeo externo. Se o visualizador começar com o vídeo do Dynamic Media Classic/Dynamic Media, use-o com esse tipo de ativo a partir de agora, não será possível carregar um vídeo externo nesse visualizador usando [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) método . E vice-versa: se o visualizador foi carregado inicialmente com vídeo externo, ele deve continuar trabalhando somente com vídeos externos.

Ao trabalhar com vídeo externo, o visualizador ignora o valor do modificador de reprodução e detecta o tipo de reprodução da extensão de vídeo externo. Se o URL de vídeo externo terminar com `.m3u8` se o visualizador estiver usando a reprodução HLS, a reprodução progressiva será usada.
