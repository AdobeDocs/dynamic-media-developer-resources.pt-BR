---
description: O visualizador suporta a reprodução de vídeo hospedado fora do Scene7 Publishing System ou AEM Dynamic Media.
seo-description: O visualizador suporta a reprodução de vídeo hospedado fora do Scene7 Publishing System ou AEM Dynamic Media.
seo-title: Suporte externo a vídeo
solution: Experience Manager
title: Suporte externo a vídeo
topic: Dynamic Media
uuid: 24739a5a-3a5d-49b8-9a15-bcf3a95fc192
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# Suporte externo a vídeo{#external-video-support}

O visualizador suporta a reprodução de vídeo hospedado fora do Scene7 Publishing System ou AEM Dynamic Media.

Os formatos suportados para o vídeo externo são MP4 no formato H.264 ou manifesto M3U8 para fluxo HLS.

O visualizador pode funcionar com vídeo do Scene7 ou Dynamic Media ou com vídeo externo. Se o visualizador start com o vídeo Scene7/Dynamic Media, use-o com esse tipo de ativo avançando, não será possível carregar um vídeo externo neste visualizador usando o método [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). E vice versa: se o visualizador foi carregado inicialmente com vídeo externo, ele deve continuar trabalhando somente com vídeos externos.

Ao trabalhar com vídeo externo, o visualizador ignora o valor do modificador de reprodução e detecta o tipo de reprodução da extensão de vídeo externa. Se o URL de vídeo externo terminar com .m3u8, o visualizador usará a reprodução HLS, caso contrário a reprodução progressiva será usada.
