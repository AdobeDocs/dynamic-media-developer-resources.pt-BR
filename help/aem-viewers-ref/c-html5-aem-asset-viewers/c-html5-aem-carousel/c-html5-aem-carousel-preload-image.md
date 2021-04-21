---
description: A imagem de pré-carregamento é uma imagem de visualização de ativo estático que é carregada logo após chamar o método init() e é exibida durante o download das bibliotecas SDK do visualizador, das informações de ativo e predefinição. A finalidade da imagem de pré-carregamento é melhorar visualmente o tempo de carregamento do visualizador e apresentar conteúdo ao usuário rapidamente.
solution: Experience Manager
title: Pré-carregar imagem
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Pré-carregar imagem{#preload-image}

A imagem de pré-carregamento é uma imagem de visualização de ativo estático que é carregada logo após chamar o método init() e é exibida durante o download das bibliotecas SDK do visualizador, das informações de ativo e predefinição. A finalidade da imagem de pré-carregamento é melhorar visualmente o tempo de carregamento do visualizador e apresentar conteúdo ao usuário rapidamente.

A imagem de pré-carregamento funciona bem para o método de incorporação do visualizador mais comum, que é a incorporação responsiva com altura irrestrita. Consulte o cabeçalho [Incorporação de design responsivo com altura irrestrita](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

No entanto, o recurso tem determinadas limitações quando outros métodos de incorporação ou opções de configuração específicas são usados. A imagem de pré-carregamento pode não ser renderizada corretamente nos seguintes casos:

* Quando o visualizador é fixado em tamanho e o tamanho é definido usando o atributo de configuração `stagesize` dentro do registro predefinido do visualizador ou no arquivo CSS do visualizador externo para o elemento do contêiner do visualizador de nível superior.
* Quando o método de incorporação de tamanho flexível com largura e altura definidas do visualizador é usado. Consulte o cabeçalho [Incorporação de tamanho flexível com largura e altura definidas](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Talvez seja necessário desativar o recurso de pré-carregamento de imagem usando o atributo de configuração `preloadImage` se estiver usando o visualizador em um dos modos de operação listados acima.

Além disso, a imagem de pré-carregamento não é usada - mesmo se ativada na configuração - se o visualizador estiver incorporado ao elemento DOM estiver oculto usando a configuração `display:none` CSS ou desconectado da árvore DOM.
