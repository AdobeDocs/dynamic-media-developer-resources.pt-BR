---
description: Há suporte para quatro tipos gerais de vinhetas de produção.
solution: Experience Manager
title: Escala de vinheta
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f9f92254-41d8-4d22-a168-78b49dd55478
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Escala de vinheta{#vignette-scaling}

Há suporte para quatro tipos gerais de vinhetas de produção.

* Resolução única

  Recomendado somente quando é certo que apenas um único tamanho de imagem de renderização é necessário.
* Várias resoluções

  Recomendado quando todos os tamanhos de imagem de renderização desejados são conhecidos. Fornece melhor qualidade e renderização mais rápida do que vinhetas de resolução única e pirâmide porque a imagem não precisa ser dimensionada após a renderização.
* Pirâmide

  Mais adequado para todas as finalidades, recomendado quando vários tamanhos de imagem são necessários e os tamanhos exatos não são predeterminados e quando o visualizador de zoom do Dynamic Media é usado.
* Pirâmide com uma ou mais resoluções adicionais

  Fornece alta qualidade para tamanhos específicos, além de flexibilidade e suporte ao visualizador de zoom.

Com efeito, cada resolução é salva na vinheta de produção como uma visualização independente, com sua própria largura e altura de imagem.

O tamanho de exibição de uma vinheta de resolução única é especificado com `-width` ou `-height`, ou ambos. Se ambos os valores forem especificados, a vinheta será dimensionada para que nenhuma das dimensões seja maior do que o tamanho especificado. Se nenhum valor for especificado, a vinheta de saída terá o mesmo tamanho que a vinheta de entrada. Nenhum aumento de escala é aplicado; se o tamanho especificado for maior que o tamanho da vinheta de entrada, a vinheta de saída terá o mesmo tamanho que a vinheta de entrada.

Efetivamente, as mesmas regras se aplicam às vinhetas de várias resoluções, com o primeiro nível de resolução sendo dimensionado como uma vinheta de resolução única. As resoluções adicionais são especificadas com valores adicionais separados por vírgula para `-width` ou `-height`. Os valores não precisam ser classificados. Se `-width` especificar vários valores, `-height` deverá fornecer apenas um único valor, e vice-versa, caso contrário, um erro será retornado.

Uma vinheta de pirâmide é criada ao especificar `-pyramid`. O maior nível de resolução de uma vinheta desse tipo é determinado exatamente como para uma vinheta de resolução única. Os níveis de resolução adicionais são determinados automaticamente por meio da escala de cada nível para 0,5x o nível anterior, com o menor nível não excedendo 128x128 pixels.

Níveis de resolução adicionais podem ser especificados para uma vinheta em pirâmide, assim como para uma vinheta de várias resoluções.
