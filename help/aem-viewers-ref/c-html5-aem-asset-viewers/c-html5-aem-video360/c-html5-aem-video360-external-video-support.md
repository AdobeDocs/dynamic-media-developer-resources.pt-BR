---
description: O visualizador suporta a reprodução de vídeo hospedado fora do Dynamic Media Classic ou AEM Dynamic Media.
solution: Experience Manager
title: Suporte externo a vídeo
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Suporte externo a vídeo{#external-video-support}

O visualizador suporta a reprodução de vídeo hospedado fora do Dynamic Media Classic ou AEM Dynamic Media.

Os formatos suportados para o vídeo externo são MP4 no formato H.264 ou manifesto M3U8 para fluxo HLS.

O visualizador pode funcionar com vídeo Dynamic Media Classic ou Dynamic Media AEM ou com vídeo externo. Se o visualizador start com o vídeo do Dynamic Media Classic/AEM Dynamic Media, ele deve ser usado com esse tipo de ativo adiante. Não é possível carregar um vídeo externo neste visualizador usando o método [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) e vice-versa. Ou seja, se o visualizador foi carregado inicialmente com vídeo externo, ele continua a funcionar somente com vídeos externos.

Ao trabalhar com vídeo externo, o visualizador ignora o valor de qualquer modificador de reprodução e detecta o tipo de reprodução da extensão de vídeo externa. Se o URL do vídeo externo terminar com `.m3u8`, o visualizador está usando a reprodução HLS; caso contrário, a reprodução progressiva será usada.
