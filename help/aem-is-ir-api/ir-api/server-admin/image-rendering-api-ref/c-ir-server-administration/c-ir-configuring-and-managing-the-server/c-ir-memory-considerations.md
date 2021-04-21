---
description: A quantidade de memória usada pela Renderização de imagem pode variar amplamente e depende muito da carga e do uso real do servidor (por exemplo, poucas vs. muitas vinhetas diferentes, tamanho e complexidade das vinhetas e assim por diante).
solution: Experience Manager
title: Considerações de memória
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# Considerações de memória{#memory-considerations}

A quantidade de memória usada pela Renderização de imagem pode variar amplamente e depende muito da carga e do uso real do servidor (por exemplo, poucas vs. muitas vinhetas diferentes, tamanho e complexidade das vinhetas e assim por diante).

Para um melhor desempenho, deve ser evitado o paginação da memória (troca).

A Renderização de imagem compartilha a gestão de memória do Servidor de imagem. Ao usar a Renderização de imagem, a memória adicional deve ser alocada. 30 a 50% da memória física pode ser razoável.

Consulte a documentação do Image Serving para obter informações sobre como alterar a alocação de memória do Image Server (ImageServer::PhysicalMemory).
