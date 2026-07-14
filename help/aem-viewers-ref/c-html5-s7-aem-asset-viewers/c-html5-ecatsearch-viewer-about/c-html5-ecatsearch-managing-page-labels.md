---
description: Gerenciamento de rótulos de página
solution: Experience Manager
title: Gerenciamento de rótulos de página
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 73c3904f-678f-47c4-b895-86671402df79
TQID: 'https://experienceleague.adobe.com/EprHC1GFDB5Lkytg4NZf8Am0myr-jXC2wxxcefelvc8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 269
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

