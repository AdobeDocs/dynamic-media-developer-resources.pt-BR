---
description: O Serviço de imagens oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP externos.
seo-description: O Serviço de imagens oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP externos.
seo-title: Fontes de imagem externas
solution: Experience Manager
title: Fontes de imagem externas
topic: Scene7 Image Serving - Image Rendering API
uuid: 28a17400-4807-4e14-937a-80309be53d55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Fontes de imagem externas{#foreign-image-sources}

O Serviço de imagens oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP externos.

Especificação de um URL externo para um comando `src=` ou `mask=` ; delimite todo o URL incorporado com chaves:

` …&src={ *[!DNL foreignUrl]*}&…`

URLs absolutos completos (se `attribute::AllowDirectUrls` estiverem definidos) e URLs relativos a `attribute::RootUrl` são permitidos. Ocorre um erro se um URL absoluto for incorporado e o atributo: `AllowDirectUrls` é 0, ou se um URL relativo é especificado e `attribute::RootUrl` está vazio.

As imagens estrangeiras são armazenadas em cache pelo servidor de acordo com os cabeçalhos de cache incluídos na resposta HTTP.
