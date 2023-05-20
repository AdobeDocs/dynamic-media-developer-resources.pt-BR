---
title: Fontes de imagem estrangeiras
description: O Servidor de imagens oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP externos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# Fontes de imagem estrangeiras{#foreign-image-sources}

O Servidor de imagens oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP externos.

Para especificar um URL externo para um `src=` ou um `mask=` ; basta delimitar todo o URL incorporado com chaves:

` …&src={ *[!DNL foreignUrl]*}&…`

URLs absolutos completos (se `attribute::AllowDirectUrls` está definido) e URLs referentes a `attribute::RootUrl` são permitidos. Ocorre um erro se um URL absoluto for incorporado e o atributo:: `AllowDirectUrls` é 0 ou se uma URL relativa for especificada e `attribute::RootUrl` está vazio.

Imagens estrangeiras são armazenadas em cache pelo servidor de acordo com os cabeçalhos de cache incluídos na resposta HTTP.
