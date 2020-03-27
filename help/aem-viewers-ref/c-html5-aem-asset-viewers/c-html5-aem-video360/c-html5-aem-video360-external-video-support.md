---
description: O visualizador suporta a reprodução de vídeo hospedado fora do SPS ou do AEM Dynamic Media.
seo-description: O visualizador suporta a reprodução de vídeo hospedado fora do SPS ou do AEM Dynamic Media.
seo-title: Suporte externo a vídeo
solution: Experience Manager
title: Suporte externo a vídeo
topic: Dynamic media
uuid: 2e9f1c54-627f-4462-ae85-8a5ca1d09762
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Suporte externo a vídeo{#external-video-support}

O visualizador suporta a reprodução de vídeo hospedado fora do SPS ou do AEM Dynamic Media.

Os formatos suportados para o vídeo externo são MP4 no formato H.264 ou manifesto M3U8 para fluxo HLS.

O visualizador pode trabalhar com vídeo do Dynamic Media Classic ou do AEM Dynamic Media ou com vídeo externo. Se o visualizador for start com o vídeo Dynamic Media Classic/AEM Dynamic Media, ele deverá ser usado com esse tipo de ativo em diante. Não é possível carregar um vídeo externo neste visualizador usando o método [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) e vice-versa. Ou seja, se o visualizador foi carregado inicialmente com vídeo externo, ele continua a funcionar somente com vídeos externos.

Ao trabalhar com vídeo externo, o visualizador ignora o valor de qualquer modificador de reprodução e detecta o tipo de reprodução da extensão de vídeo externa. Se o URL do vídeo externo terminar com `.m3u8`, o visualizador usará a reprodução HLS; caso contrário, a reprodução progressiva será usada.
