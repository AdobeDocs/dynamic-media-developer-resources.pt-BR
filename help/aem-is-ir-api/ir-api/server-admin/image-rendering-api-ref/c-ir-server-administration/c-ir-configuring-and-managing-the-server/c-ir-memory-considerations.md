---
description: A quantidade de memória usada pela Renderização de imagem pode variar amplamente e depende muito da carga e do uso real do servidor (por exemplo, poucas vs. muitas vinhetas diferentes, tamanho e complexidade das vinhetas e assim por diante).
solution: Experience Manager
title: Considerações de memória
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Considerações de memória{#memory-considerations}

A quantidade de memória usada pela Renderização de imagem pode variar amplamente e depende muito da carga e do uso real do servidor (por exemplo, poucas vs. muitas vinhetas diferentes, tamanho e complexidade das vinhetas e assim por diante).

Para um melhor desempenho, deve ser evitado o paginação da memória (troca).

A Renderização de imagem compartilha a gestão de memória do Servidor de imagem. Ao usar a Renderização de imagem, a memória adicional deve ser alocada. 30 a 50% da memória física pode ser razoável.

Consulte a documentação do Image Serving para obter informações sobre como alterar a alocação de memória do Image Server (ImageServer::PhysicalMemory).
