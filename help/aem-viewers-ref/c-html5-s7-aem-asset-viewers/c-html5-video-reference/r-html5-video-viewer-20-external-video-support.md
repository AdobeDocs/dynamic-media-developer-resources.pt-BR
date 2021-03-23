---
description: O visualizador suporta a reprodução de vídeo hospedado fora do Dynamic Media Classic ou AEM Dynamic Media.
solution: Experience Manager
title: Suporte a vídeo externo
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# Suporte a vídeo externo{#external-video-support}

O visualizador suporta a reprodução de vídeo hospedado fora do Dynamic Media Classic ou AEM Dynamic Media.

Os formatos suportados para o vídeo externo são MP4 no formato H.264 ou manifesto M3U8 para fluxo HLS.

O visualizador pode trabalhar com vídeo do Dynamic Media Classic ou AEM Dynamic Media ou com vídeo externo. Se o visualizador começar com o vídeo do Dynamic Media Classic/Dynamic Media, use-o com esse tipo de ativo a partir de agora, não será possível carregar um vídeo externo nesse visualizador usando o método [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). E vice-versa: se o visualizador foi carregado inicialmente com vídeo externo, ele deve continuar trabalhando somente com vídeos externos.

Ao trabalhar com vídeo externo, o visualizador ignora o valor do modificador de reprodução e detecta o tipo de reprodução da extensão de vídeo externo. Se o URL do vídeo externo terminar com .m3u8, o visualizador estará usando a reprodução HLS, caso contrário a reprodução progressiva será usada.
