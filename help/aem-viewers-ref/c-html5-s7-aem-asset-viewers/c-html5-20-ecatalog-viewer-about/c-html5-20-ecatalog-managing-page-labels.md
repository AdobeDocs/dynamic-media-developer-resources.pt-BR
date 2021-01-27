---
description: Gerenciamento de rótulos de página
solution: Experience Manager
title: Gerenciamento de rótulos de página
topic: Dynamic Media
uuid: ab3df37d-113b-4762-ba9c-b92ffc41f1a2
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# Gerenciar rótulos de página{#managing-page-labels}

Há dois lugares na interface do usuário do visualizador onde os rótulos de página são mostrados: modo de miniaturas e o menu suspenso do sumário.

Há três tipos de rótulos que podem ser definidos:

* Etiquetas definidas pelo autor usando o mecanismo de localização SYMBOL.
* Rótulos definidos pelo autor no backend, no Dynamic Media Classic.
* Rótulos gerados automaticamente pelo visualizador.

Os rótulos baseados em SYMBOL são definidos usando `MediaSet.LABEL_XX[_YY]` e `MediaSet.LABEL_DELIM` SYMBOLs conforme descrito em [Localização de elementos da interface do usuário](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). Você pode definir esses rótulos para toda a propagação do catálogo eletrônico, caso em que você deve usar a sintaxe SYMBOL curta ( `MediaSet.LABEL_XX`). Ou especifique-o para cada página individualmente usando a sintaxe SYMBOL completa ( `MediaSet.LABEL_XX_YY`).

Quando você define rótulos para ambas as páginas na página espelhada do catálogo eletrônico, o visualizador concatena esses rótulos em uma sequência usando `MediaSet.LABEL_DELIM` SYMBOL. Rótulos baseados em SYMBOL têm prioridade sobre rótulos que são definidos no backend ou gerados automaticamente pelo visualizador.

Os rótulos definidos no Dynamic Media Classic são armazenados no registro UserData de imagens individuais de páginas. Igual aos rótulos baseados em SYMBOL. Ou seja, se ambas as páginas na página espelhada do catálogo eletrônico tiverem rótulos definidos, elas serão concatenadas usando `MediaSet.LABEL_DELIM` SYMBOL no modo paisagem. Os rótulos do Dynamic Media Classic têm prioridade sobre os rótulos gerados automaticamente, mas são substituídos por rótulos baseados em SYMBOL.

Rótulos gerados automaticamente são números sequenciais atribuídos a todas as páginas no catálogo eletrônico. Rótulos gerados automaticamente são ignorados para a propagação em questão se ela tiver rótulos baseados em SYMBOL definidos ou rótulos do Dynamic Media Classic definidos.

No sumário, é possível desativar a exibição de rótulos gerados automaticamente usando o parâmetro `showdefault`.
