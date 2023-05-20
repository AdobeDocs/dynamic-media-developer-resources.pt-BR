---
title: Suporte a vídeo externo
description: O visualizador é compatível com a reprodução de vídeo hospedado fora do Dynamic Media Classic ou Adobe Experience Manager - Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Suporte a vídeo externo{#external-video-support}

O visualizador é compatível com a reprodução de vídeo hospedado fora do Dynamic Media Classic ou Adobe Experience Manager - Dynamic Media.

Os formatos compatíveis com o vídeo externo são MP4 no formato H.264 ou manifesto M3U8 para fluxo HLS.

O visualizador pode trabalhar com vídeo Dynamic Media Classic ou Experience Manager - Dynamic Media ou com vídeo externo. Se o visualizador começar com vídeo do Dynamic Media Classic/Dynamic Media, usá-lo com esse tipo de ativo daqui para frente, não será possível carregar um vídeo externo nesse visualizador usando [`setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) método. E vice-versa: se o visualizador foi carregado inicialmente com vídeo externo, ele deve continuar trabalhando somente com vídeos externos.

Ao trabalhar com vídeo externo, o visualizador ignora o valor do modificador de reprodução e detecta o tipo de reprodução da extensão de vídeo externa. Se o URL do vídeo externo terminar com `.M3U8` o visualizador está usando a reprodução HLS, caso contrário, a reprodução progressiva é usada.
