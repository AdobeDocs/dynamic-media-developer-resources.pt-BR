---
description: O Image Serving oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP estrangeiros.
solution: Experience Manager
title: Fontes de imagem externas
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Fontes de imagem externas{#foreign-image-sources}

O Image Serving oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP estrangeiros.

Especificar um URL externo para um comando `src=` ou `mask=`; delimite todo o URL incorporado com chaves:

` …&src={ *[!DNL foreignUrl]*}&…`

URLs absolutos completos (se `attribute::AllowDirectUrls` estiver definido) e URLs relativos a `attribute::RootUrl` são permitidos. Um erro ocorre se um URL absoluto for incorporado e o atributo : `AllowDirectUrls` é 0 ou se um URL relativo é especificado e `attribute::RootUrl` está vazio.

Imagens estrangeiras são armazenadas em cache pelo servidor de acordo com os cabeçalhos de cache incluídos na resposta HTTP.
