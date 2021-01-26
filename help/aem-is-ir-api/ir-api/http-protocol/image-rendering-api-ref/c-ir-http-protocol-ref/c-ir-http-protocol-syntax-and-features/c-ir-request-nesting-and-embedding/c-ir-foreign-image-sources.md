---
description: O Serviço de imagens oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP externos.
seo-description: O Serviço de imagens oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP externos.
seo-title: Fontes de imagem externas
solution: Experience Manager
title: Fontes de imagem externas
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 28a17400-4807-4e14-937a-80309be53d55
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# Fontes de imagem externas{#foreign-image-sources}

O Serviço de imagens oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP externos.

Para especificar um URL externo para um comando `src=` ou `mask=`; delimite todo o URL incorporado com chaves:

` …&src={ *[!DNL foreignUrl]*}&…`

URLs absolutos completos (se `attribute::AllowDirectUrls` estiver definido) e URLs relativos a `attribute::RootUrl` serão permitidos. Ocorre um erro se um URL absoluto for incorporado e o atributo: `AllowDirectUrls` é 0, ou se um URL relativo é especificado e `attribute::RootUrl` está vazio.

As imagens estrangeiras são armazenadas em cache pelo servidor de acordo com os cabeçalhos de cache incluídos na resposta HTTP.
