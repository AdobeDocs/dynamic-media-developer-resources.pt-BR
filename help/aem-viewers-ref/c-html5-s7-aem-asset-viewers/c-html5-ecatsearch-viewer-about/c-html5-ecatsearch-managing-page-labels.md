---
description: Gerenciamento de rótulos de página
solution: Experience Manager
title: Gerenciamento de rótulos de página
uuid: 49444fe6-ef34-4e5b-a293-e23830a67b4d
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---


# Gerenciar rótulos de página{#managing-page-labels}

Há dois lugares na interface do usuário do visualizador em que os rótulos de página são mostrados: modo de miniaturas e o menu suspenso de índice.

Há três tipos de rótulos que podem ser definidos:

* Rótulos definidos pelo autor usando o mecanismo de localização SYMBOL.
* Rótulos definidos pelo autor no backend, dentro do Dynamic Media Classic.
* Rótulos gerados automaticamente pelo visualizador.

Os rótulos baseados em SYMBOL são definidos usando `MediaSet.LABEL_XX[_YY]` e `MediaSet.LABEL_DELIM` SYMBOLs, conforme descrito em [Localização dos elementos da interface do usuário](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). Você pode definir esses rótulos para todo o spread do catálogo eletrônico, nesse caso, você deve usar a sintaxe SYMBOL curta ( `MediaSet.LABEL_XX`). Ou especifique-o para cada página individualmente usando a sintaxe SYMBOL completa ( `MediaSet.LABEL_XX_YY`).

Quando você define rótulos para ambas as páginas no spread do catálogo eletrônico, o visualizador concatena esses rótulos em uma cadeia de caracteres usando `MediaSet.LABEL_DELIM` SYMBOL. Os rótulos baseados em SYMBOL têm prioridade sobre os rótulos que são definidos no backend ou os rótulos gerados automaticamente pelo visualizador.

Rótulos definidos no Dynamic Media Classic são armazenados no registro UserData de imagens de página individuais. O mesmo que com rótulos baseados em SYMBOL. Ou seja, se ambas as páginas no spread do catálogo eletrônico tiverem rótulos definidos, elas serão concatenadas usando `MediaSet.LABEL_DELIM` SYMBOL no modo paisagem. Os rótulos do Dynamic Media Classic têm prioridade sobre os rótulos gerados automaticamente, mas são substituídos por rótulos baseados em SYMBOL.

Os rótulos gerados automaticamente são números sequenciais atribuídos a todas as páginas no catálogo eletrônico. Os rótulos gerados automaticamente são ignorados para o spread fornecido se ele tiver rótulos baseados em SYMBOL definidos ou rótulos do Dynamic Media Classic definidos.

No índice, é possível desativar a exibição de rótulos gerados automaticamente usando o parâmetro `showdefault` .
