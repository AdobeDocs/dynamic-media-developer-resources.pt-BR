---
description: Gerenciamento de rótulos de página
solution: Experience Manager
title: Gerenciamento de rótulos de página
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 73c3904f-678f-47c4-b895-86671402df79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Gerenciamento de rótulos de página{#managing-page-labels}

Há dois lugares na interface do usuário do visualizador em que os rótulos da página são exibidos: o modo de miniaturas e o menu suspenso de índice.

Há três tipos de rótulos que podem ser definidos:

* Rótulos definidos pelo autor usando o mecanismo de localização SYMBOL.
* Rótulos definidos pelo autor no back-end, dentro do Dynamic Media Classic.
* Rótulos gerados automaticamente pelo visualizador.

Os rótulos baseados em SYMBOL são definidos usando `MediaSet.LABEL_XX[_YY]` e `MediaSet.LABEL_DELIM` SYMBOLs conforme descrito em [Localização dos elementos da interface do usuário](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). Você pode definir esses rótulos para toda a disseminação do catálogo eletrônico, nesse caso, você deve usar a sintaxe SYMBOL curta ( `MediaSet.LABEL_XX`). Ou especifique para cada página individualmente usando a sintaxe SYMBOL completa ( `MediaSet.LABEL_XX_YY`).

Quando você define rótulos para ambas as páginas na página espelhada ecatalog, o visualizador concatena esses rótulos em uma cadeia de caracteres usando `MediaSet.LABEL_DELIM` SYMBOL. Os rótulos baseados em SÍMBOLOS têm prioridade sobre os rótulos definidos no back-end ou gerados automaticamente pelo visualizador.

Os rótulos definidos no Dynamic Media Classic são armazenados no registro UserData de imagens de páginas individuais. O mesmo que com os rótulos baseados em SÍMBOLO. Ou seja, se ambas as páginas da página espelhada ecatalog tiverem rótulos definidos, eles serão concatenados usando o `MediaSet.LABEL_DELIM` SYMBOL no modo paisagem. Os rótulos do Dynamic Media Classic têm prioridade sobre os rótulos gerados automaticamente, mas são substituídos por rótulos baseados em SÍMBOLO.

Os rótulos gerados automaticamente são números sequenciais atribuídos a todas as páginas no catálogo eletrônico. Os rótulos gerados automaticamente são ignorados para a página espelhada fornecida se ela tiver rótulos baseados em SÍMBOLO definidos ou rótulos Dynamic Media Classic definidos.

No índice, é possível desabilitar a exibição de rótulos gerados automaticamente usando o parâmetro `showdefault`.
