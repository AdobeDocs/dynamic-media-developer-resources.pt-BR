---
description: Há suporte para quatro tipos gerais de vinhetas de produção.
solution: Experience Manager
title: Escala de vinheta
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f9f92254-41d8-4d22-a168-78b49dd55478
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Escala de vinheta{#vignette-scaling}

Há suporte para quatro tipos gerais de vinhetas de produção.

* Resolução única

   Recomendado somente quando tiver certeza de que apenas um único tamanho de imagem de renderização é necessário.
* Multiresolução

   Recomendado quando todos os tamanhos de imagem de renderização desejados forem conhecidos. Fornece melhor qualidade e renderização mais rápida do que vinhetas de resolução única e pirâmide, pois a imagem não precisa ser dimensionada após a renderização.
* Pirâmide

   Melhor propósito, recomendado quando são necessários vários tamanhos de imagem e os tamanhos exatos não são predeterminados e quando o visualizador de Zoom do Dynamic Media é usado.
* Pirâmide com uma ou mais resoluções adicionais

   Fornece alta qualidade para tamanhos específicos e ainda oferece flexibilidade e suporte para visualizadores de zoom.

Na verdade, cada resolução é salva na vinheta de produção como uma exibição independente com sua própria largura e altura da imagem.

O tamanho de exibição de uma vinheta de resolução única é especificado com `-width` ou `-height` ou ambos. Se ambos os valores forem especificados, a vinheta será dimensionada para que nenhuma das dimensões seja maior do que o tamanho especificado. Se nenhum dos valores for especificado, a vinheta de saída terá o mesmo tamanho da vinheta de entrada. Não se aplica qualquer aumento; se o tamanho especificado for maior que o tamanho da vinheta de entrada, a vinheta de saída terá o mesmo tamanho da vinheta de entrada.

Com efeito, as mesmas regras aplicam-se às vinhetas multiresolução, com o primeiro nível de resolução a ser dimensionado como uma vinheta de resolução única. As resoluções adicionais são especificadas com valores separados por vírgula adicionais para `-width` ou `-height`. Os valores não precisam ser classificados. If `-width` especifica vários valores e `-height` O deve fornecer apenas um valor, e vice-versa, caso contrário, um erro será retornado.

Uma vinheta de pirâmide é criada ao especificar `-pyramid`. O maior nível de resolução de uma vinheta desse tipo é determinado exatamente como para uma vinheta de resolução única. Os níveis de resolução adicionais são determinados automaticamente por meio do dimensionamento de cada nível para 0,5x o nível anterior, com o menor nível não superior a 128x128 pixels.

Níveis de resolução adicionais podem ser especificados para uma vinheta pirâmide, como para uma vinheta multiresolução.
