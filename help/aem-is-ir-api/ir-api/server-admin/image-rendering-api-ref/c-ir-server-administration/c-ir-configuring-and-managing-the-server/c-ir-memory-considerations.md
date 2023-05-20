---
description: A quantidade de memória usada pela Renderização de imagem pode variar muito e depende muito da carga e do uso real do servidor (por exemplo, poucas vinhetas versus muitas diferentes, tamanho e complexidade das vinhetas e assim por diante).
solution: Experience Manager
title: Considerações sobre memória
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# Considerações sobre memória{#memory-considerations}

A quantidade de memória usada pela Renderização de imagem pode variar muito e depende muito da carga e do uso real do servidor (por exemplo, poucas vinhetas versus muitas diferentes, tamanho e complexidade das vinhetas e assim por diante).

Para obter o melhor desempenho, a paginação de memória (troca) deve ser evitada.

A Renderização de imagem compartilha o gerenciamento de memória do Servidor de imagens. Ao usar a Renderização de imagem, deve ser alocada memória adicional. 30 a 50% da memória física pode ser razoável.

Consulte a documentação do Servidor de imagens para obter informações sobre como alterar a alocação de memória do Servidor de imagens (ImageServer::PhysicalMemory).
