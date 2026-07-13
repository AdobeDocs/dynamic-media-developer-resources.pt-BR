---
description: A quantidade de memória usada pela Renderização de imagem pode variar muito e depende muito da carga e do uso real do servidor (por exemplo, poucas vinhetas versus muitas diferentes, tamanho e complexidade das vinhetas e assim por diante).
solution: Experience Manager
title: Considerações sobre memória
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
TQID: 'https://experienceleague.adobe.com/l41dx4mMn82TvImVVCJJKgJZbP-mWT5KbnzfZ5xFJqg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 129
ht-degree: 0%

---

# Considerações sobre memória{#memory-considerations}

A quantidade de memória usada pela Renderização de imagem pode variar muito e depende muito da carga e do uso real do servidor (por exemplo, poucas vinhetas versus muitas diferentes, tamanho e complexidade das vinhetas e assim por diante).

Para obter o melhor desempenho, a paginação de memória (troca) deve ser evitada.

A Renderização de imagem compartilha o gerenciamento de memória do Servidor de imagens. Ao usar a Renderização de imagem, deve ser alocada memória adicional. 30 a 50% da memória física pode ser razoável.

Consulte a documentação do Servidor de imagens para obter informações sobre como alterar a alocação de memória do Servidor de imagens (ImageServer::PhysicalMemory).

