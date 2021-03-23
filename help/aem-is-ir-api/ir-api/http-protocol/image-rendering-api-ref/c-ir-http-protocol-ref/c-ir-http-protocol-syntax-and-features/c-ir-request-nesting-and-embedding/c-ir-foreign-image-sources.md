---
description: O Image Serving oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP estrangeiros.
seo-description: O Image Serving oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP estrangeiros.
seo-title: Fontes de imagem externas
solution: Experience Manager
title: Fontes de imagem externas
uuid: 28a17400-4807-4e14-937a-80309be53d55
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# Fontes de imagem externas{#foreign-image-sources}

O Image Serving oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP estrangeiros.

Especificar um URL externo para um comando `src=` ou `mask=`; delimite todo o URL incorporado com chaves:

` …&src={ *[!DNL foreignUrl]*}&…`

URLs absolutos completos (se `attribute::AllowDirectUrls` estiver definido) e URLs relativos a `attribute::RootUrl` são permitidos. Um erro ocorre se um URL absoluto for incorporado e o atributo : `AllowDirectUrls` é 0 ou se um URL relativo é especificado e `attribute::RootUrl` está vazio.

Imagens estrangeiras são armazenadas em cache pelo servidor de acordo com os cabeçalhos de cache incluídos na resposta HTTP.
