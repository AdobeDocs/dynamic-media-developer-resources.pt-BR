---
title: Suporte a vídeo externo
description: O visualizador aceita a reprodução de vídeo hospedado fora do Dynamic Media Classic ou Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Suporte a vídeo externo{#external-video-support}

O visualizador aceita a reprodução de vídeo hospedado fora do Dynamic Media Classic ou Adobe Experience Manager, Dynamic Media.

Os formatos suportados para o vídeo externo são MP4 no formato H.264 ou manifesto M3U8 para fluxo HLS.

O visualizador pode trabalhar com vídeo Dynamic Media Classic ou Experience Manager Dynamic Media ou com vídeo externo. Se o visualizador começar com o vídeo do Dynamic Media Classic/AEM Dynamic Media, ele deverá ser usado com esse tipo de ativo a partir de agora. Não é possível carregar um vídeo externo nesse visualizador usando o método [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) e vice-versa. Ou seja, se o visualizador foi carregado inicialmente com vídeo externo, ele continua a funcionar somente com vídeos externos.

Ao trabalhar com vídeo externo, o visualizador ignora o valor de qualquer modificador de reprodução e detecta o tipo de reprodução da extensão de vídeo externo. Se o URL do vídeo externo terminar com `.m3u8`, o visualizador estará usando a reprodução de HLS; caso contrário, a reprodução progressiva será usada.
