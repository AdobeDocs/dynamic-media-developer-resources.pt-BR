---
description: Há suporte para quatro tipos gerais de vinhetas de produção.
seo-description: Há suporte para quatro tipos gerais de vinhetas de produção.
seo-title: Escala de vinheta
solution: Experience Manager
title: Escala de vinheta
topic: Scene7 Image Serving - Image Rendering API
uuid: 08c8f826-7dce-4bcb-9323-4892262eb578
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---


# Escala de vinheta{#vignette-scaling}

Há suporte para quatro tipos gerais de vinhetas de produção.

* Resolução única

   Recomendado somente quando estiver certo de que apenas um tamanho de imagem de renderização é necessário.
* Multiresolução

   Recomendado quando todos os tamanhos de imagem de renderização desejados forem conhecidos. Oferece melhor qualidade e renderização mais rápida do que vinhetas de resolução única e pirâmide, pois a imagem não precisa ser dimensionada após a renderização.
* Pirâmide

   Melhor finalidade, recomendada quando vários tamanhos de imagem são necessários e os tamanhos exatos não são predeterminados e quando um dos visualizadores de zoom do Flash Scene7 é usado.
* Pirâmide com uma ou mais resoluções adicionais

   Oferece alta qualidade para tamanhos específicos e ainda oferece flexibilidade e suporte para o visualizador de zoom.

Efetivamente, cada resolução é salva na vinheta de produção como uma visualização independente com sua própria largura e altura de imagem.

O tamanho de visualização de uma vinheta de resolução única é especificado com `-width` ou `-height` ou ambos. Se ambos os valores forem especificados, a vinheta será dimensionada para que nenhuma das dimensões seja maior que o tamanho especificado. Se nenhum dos valores for especificado, a vinheta de saída terá o mesmo tamanho que a vinheta de entrada. Não será aplicado qualquer aumento; se o tamanho especificado for maior que o tamanho da vinheta de entrada, a vinheta de saída terá o mesmo tamanho que a vinheta de entrada.

Com efeito, as mesmas regras aplicam-se às vinhetas de resolução múltipla, sendo o primeiro nível de resolução dimensionado como uma vinheta de resolução única. As resoluções adicionais são especificadas com valores separados por vírgulas adicionais para `-width` ou `-height`. Os valores não precisam ser classificados. Se `-width` especificar vários valores, `-height` deverá fornecer apenas um único valor, e vice-versa, caso contrário, um erro será retornado.

Uma vinheta pirâmide é criada especificando `-pyramid`. O nível de resolução mais elevado de uma vinheta deste tipo é determinado exatamente como para uma vinheta de resolução única. Os níveis de resolução adicionais são determinados automaticamente por meio do dimensionamento de cada nível para 0,5x o nível anterior, com o menor nível não superior a 128x128 pixels.

Níveis de resolução adicionais podem ser especificados para uma vinheta pirâmide, assim como para uma vinheta multiresolução.
