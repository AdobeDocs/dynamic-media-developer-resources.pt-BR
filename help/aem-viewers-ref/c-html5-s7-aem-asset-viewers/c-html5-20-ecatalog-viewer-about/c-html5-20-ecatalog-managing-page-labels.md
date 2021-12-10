---
title: Gerenciamento de rótulos de página
description: Gerenciamento de rótulos de página
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b62b5cb8-6100-4d0f-afd8-e6daa6ce6539
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Gerenciamento de rótulos de página{#managing-page-labels}

Há dois lugares na interface do usuário do visualizador em que os rótulos de página são mostrados: modo de miniaturas e o menu suspenso de índice.

Há três tipos de rótulos que podem ser definidos:

* Rótulos definidos pelo autor usando o mecanismo de localização SYMBOL.
* Rótulos definidos pelo autor no backend, dentro do Dynamic Media Classic.
* Rótulos gerados automaticamente pelo visualizador.

Os rótulos baseados em SYMBOL são definidos usando `MediaSet.LABEL_XX[_YY]` e `MediaSet.LABEL_DELIM` SYMBOLs conforme descrito em [Localização dos elementos da interface do usuário](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). Você pode definir esses rótulos para todo o spread do catálogo eletrônico, nesse caso, você deve usar a sintaxe SYMBOL curta ( `MediaSet.LABEL_XX`). Ou especifique-o para cada página individualmente usando a sintaxe SYMBOL completa ( `MediaSet.LABEL_XX_YY`).

Quando você define rótulos para ambas as páginas na distribuição do catálogo eletrônico, o visualizador concatena esses rótulos em uma sequência usando `MediaSet.LABEL_DELIM` SÍMBOLO. Os rótulos baseados em SYMBOL têm prioridade sobre os rótulos que são definidos no backend ou os rótulos gerados automaticamente pelo visualizador.

Rótulos definidos no Dynamic Media Classic são armazenados no registro UserData de imagens individuais da página. O mesmo que com rótulos baseados em SYMBOL. Ou seja, se ambas as páginas no catálogo eletrônico têm rótulos definidos, eles são concatenados usando `MediaSet.LABEL_DELIM` SYMBOL no modo paisagem. Os rótulos Dynamic Media Classic têm prioridade sobre os rótulos gerados automaticamente, mas são substituídos por rótulos baseados em SYMBOL.

Os rótulos gerados automaticamente são números sequenciais atribuídos a todas as páginas no catálogo eletrônico. Os rótulos gerados automaticamente são ignorados para o spread fornecido se ele tiver rótulos baseados em SYMBOL definidos ou rótulos Dynamic Media Classic definidos.

No índice, é possível desativar a exibição de rótulos gerados automaticamente usando `showdefault` parâmetro.
