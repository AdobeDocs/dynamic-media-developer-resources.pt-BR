---
title: Fontes de imagem estrangeiras
description: O Servidor de imagens oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP externos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
TQID: 'https://experienceleague.adobe.com/doS6fbVfaXGtLVNBAmOkB-TquNmOc5B2B--IewouFDY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 0%

---

# Fontes de imagem estrangeiras{#foreign-image-sources}

O Servidor de imagens oferece suporte ao acesso a imagens de origem em servidores HTTP e FTP externos.

Para especificar uma URL externa para um comando `src=` ou `mask=`; basta delimitar toda a URL incorporada com chaves:

` …&src={ *[!DNL foreignUrl]*}&…`

URLs absolutos completos (se `attribute::AllowDirectUrls` estiver definido) e URLs relativos a `attribute::RootUrl` são permitidos. Erro se uma URL absoluta estiver inserida e o atributo: `AllowDirectUrls` for 0, ou se uma URL relativa for especificada e `attribute::RootUrl` estiver vazia.

Imagens estrangeiras são armazenadas em cache pelo servidor de acordo com os cabeçalhos de cache incluídos na resposta HTTP.

