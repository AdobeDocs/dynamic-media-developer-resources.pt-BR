---
title: Fontes de imagem estrangeiras
description: O Servidor de imagens oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP externos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Fontes de imagem estrangeiras{#foreign-image-sources}

O Servidor de imagens oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP externos.

Para especificar uma URL externa para um comando `src=` ou `mask=`; basta delimitar toda a URL incorporada com chaves:

` …&src={ *[!DNL foreignUrl]*}&…`

URLs absolutos completos (se `attribute::AllowDirectUrls` estiver definido) e URLs relativos a `attribute::RootUrl` são permitidos. Erro se uma URL absoluta estiver inserida e o atributo: `AllowDirectUrls` for 0, ou se uma URL relativa for especificada e `attribute::RootUrl` estiver vazia.

Imagens estrangeiras são armazenadas em cache pelo servidor de acordo com os cabeçalhos de cache incluídos na resposta HTTP.
