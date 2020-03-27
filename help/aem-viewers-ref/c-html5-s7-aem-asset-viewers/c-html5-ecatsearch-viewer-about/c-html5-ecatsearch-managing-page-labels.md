---
description: nulo
seo-description: nulo
seo-title: Gerenciamento de rótulos de página
solution: Experience Manager
title: Gerenciamento de rótulos de página
topic: Dynamic media
uuid: 49444fe6-ef34-4e5b-a293-e23830a67b4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Gerenciamento de rótulos de página{#managing-page-labels}

Há dois lugares na interface do usuário do visualizador onde os rótulos de página são mostrados: modo de miniaturas e o menu suspenso do sumário.

Há três tipos de rótulos que podem ser definidos:

* Etiquetas definidas pelo autor usando o mecanismo de localização SYMBOL.
* Rótulos definidos pelo autor no backend, dentro do Scene7 Publishing System.
* Rótulos gerados automaticamente pelo visualizador.

As etiquetas baseadas em SYMBOL são definidas usando `MediaSet.LABEL_XX[_YY]` e `MediaSet.LABEL_DELIM` SYMBOLs, conforme descrito em [Localização de elementos](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)da interface do usuário. Você pode definir esses rótulos para toda a distribuição do catálogo eletrônico, caso em que você deve usar a sintaxe SYMBOL curta ( `MediaSet.LABEL_XX`). Ou especifique-o para cada página individualmente usando a sintaxe completa SYMBOL ( `MediaSet.LABEL_XX_YY`).

Quando você define rótulos para ambas as páginas na página espelhada do catálogo eletrônico, o visualizador concatena esses rótulos em uma sequência usando `MediaSet.LABEL_DELIM` SYMBOL. Rótulos baseados em SYMBOL têm prioridade sobre rótulos que são definidos no backend ou gerados automaticamente pelo visualizador.

Os rótulos definidos no Scene7 Publishing System são armazenados no registro UserData de imagens individuais de páginas. Igual aos rótulos baseados em SYMBOL. Ou seja, se ambas as páginas na página espelhada do ecatalog tiverem rótulos definidos, elas serão concatenadas usando `MediaSet.LABEL_DELIM` SYMBOL no modo paisagem. Os rótulos do Scene7 Publishing System têm prioridade sobre os rótulos gerados automaticamente, mas são substituídos por rótulos baseados em SYMBOL.

Rótulos gerados automaticamente são números sequenciais atribuídos a todas as páginas no catálogo eletrônico. Rótulos gerados automaticamente são ignorados para a propagação específica se ela tiver rótulos baseados em SYMBOL definidos ou rótulos do Scene7 Publishing System definidos.

No sumário, é possível desativar a exibição de rótulos gerados automaticamente usando o `showdefault` parâmetro.
