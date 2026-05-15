---
title: Suporte a vídeo externo
description: O visualizador é compatível com a reprodução de vídeo hospedado fora do Dynamic Media Classic ou Adobe Experience Manager - Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
TQID: 'https://experienceleague.adobe.com/HymmuAHcdNoNLbGyF0k0jo6ZQfIaPPEjy6w34GuNWZI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 0%

---

# Suporte a vídeo externo{#external-video-support}

O visualizador é compatível com a reprodução de vídeo hospedado fora do Dynamic Media Classic ou Adobe Experience Manager - Dynamic Media.

Os formatos compatíveis com o vídeo externo são MP4 no formato H.264 ou manifesto M3U8 para fluxo do HLS.

O visualizador pode trabalhar com vídeo do Dynamic Media Classic ou do Experience Manager - Dynamic Media ou com vídeo externo. Se o visualizador começar com vídeo do Dynamic Media Classic/Dynamic Media, usá-lo com esse tipo de ativo daqui para frente, não será possível carregar um vídeo externo nesse visualizador usando o método [`setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). E vice-versa: se o visualizador foi carregado inicialmente com vídeo externo, ele deve continuar trabalhando somente com vídeos externos.

Ao trabalhar com vídeo externo, o visualizador ignora o valor do modificador de reprodução e detecta o tipo de reprodução da extensão de vídeo externa. Se a URL externa do vídeo terminar com `.m3u8` o visualizador estiver usando a reprodução de HLS; caso contrário, a reprodução progressiva será usada.
