---
title: Fontes de imagem externas
description: O Image Serving oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP estrangeiros.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# Fontes de imagem externas{#foreign-image-sources}

O Image Serving oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP estrangeiros.

Especificação de um URL externo para um `src=` ou `mask=` comando; delimite todo o URL incorporado com chaves:

` …&src={ *[!DNL foreignUrl]*}&…`

URLs absolutos completos (se `attribute::AllowDirectUrls` é definido) e URLs relativos a `attribute::RootUrl` são permitidas. Um erro ocorre se um URL absoluto for incorporado e o atributo : `AllowDirectUrls` for 0 ou se um URL relativo for especificado e `attribute::RootUrl` está vazio.

Imagens estrangeiras são armazenadas em cache pelo servidor de acordo com os cabeçalhos de cache incluídos na resposta HTTP.
