---
description: O Image Serving oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP estrangeiros.
solution: Experience Manager
title: Fontes de imagem externas
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# Fontes de imagem externas{#foreign-image-sources}

O Image Serving oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP estrangeiros.

Especificar um URL externo para um comando `src=` ou `mask=`; delimite todo o URL incorporado com chaves:

` …&src={ *[!DNL foreignUrl]*}&…`

URLs absolutos completos (se `attribute::AllowDirectUrls` estiver definido) e URLs relativos a `attribute::RootUrl` são permitidos. Um erro ocorre se um URL absoluto for incorporado e o atributo : `AllowDirectUrls` é 0 ou se um URL relativo é especificado e `attribute::RootUrl` está vazio.

Imagens estrangeiras são armazenadas em cache pelo servidor de acordo com os cabeçalhos de cache incluídos na resposta HTTP.
