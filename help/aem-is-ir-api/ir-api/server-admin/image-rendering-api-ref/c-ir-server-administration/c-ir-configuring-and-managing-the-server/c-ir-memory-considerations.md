---
description: A quantidade de memória usada pela Renderização de imagem pode variar amplamente e depende muito da carga e do uso reais do servidor (por exemplo, poucas ou muitas vinhetas diferentes, tamanho e complexidade das vinhetas, etc).
seo-description: A quantidade de memória usada pela Renderização de imagem pode variar amplamente e depende muito da carga e do uso reais do servidor (por exemplo, poucas ou muitas vinhetas diferentes, tamanho e complexidade das vinhetas, etc).
seo-title: Considerações de memória
solution: Experience Manager
title: Considerações de memória
topic: Scene7 Image Serving - Image Rendering API
uuid: 21247081-ff27-4237-93da-5fc996417dfd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Considerações de memória{#memory-considerations}

A quantidade de memória usada pela Renderização de imagem pode variar amplamente e depende muito da carga e do uso reais do servidor (por exemplo, poucas ou muitas vinhetas diferentes, tamanho e complexidade das vinhetas, etc).

Para obter o melhor desempenho, deve evitar-se a paginação da memória (troca).

A Renderização de imagem compartilha o gerenciamento de memória do Servidor de imagens. Ao usar a renderização de imagem, memória adicional deve ser alocada. 30 a 50% da memória física pode ser razoável.

Consulte a documentação do Servidor de imagens para obter informações sobre como alterar a alocação de memória do Servidor de imagens (ImageServer::PhysicalMemory).
