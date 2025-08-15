---
title: Pré-carregar imagem
description: A imagem pré-carregada é uma imagem de pré-visualização de ativo estático que é carregada logo após chamar o método init() e é exibida enquanto as bibliotecas, os ativos e as informações predefinidas do SDK do Viewer são baixados. O objetivo do pré-carregamento da imagem é melhorar visualmente o tempo de carregamento do visualizador e apresentar conteúdo ao usuário rapidamente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Pré-carregar imagem{#preload-image}

A imagem pré-carregada é uma imagem de pré-visualização de ativo estático que é carregada logo após chamar o método init() e é exibida enquanto as bibliotecas, os ativos e as informações predefinidas do SDK do Viewer são baixados. O objetivo do pré-carregamento da imagem é melhorar visualmente o tempo de carregamento do visualizador e apresentar conteúdo ao usuário rapidamente.

O pré-carregamento de imagens funciona bem para o método de incorporação do visualizador mais comum, que é a incorporação responsiva com altura irrestrita. Consulte o cabeçalho [Incorporação responsiva de design com altura irrestrita](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

No entanto, o recurso tem determinadas limitações quando outros métodos de incorporação ou opções de configuração específicas são usados. A imagem pré-carregada pode não ser renderizada corretamente nos seguintes casos:

* Quando o visualizador é fixo em tamanho e o tamanho é definido usando o atributo de configuração `stagesize` dentro do registro de predefinição do visualizador. Ou, usando o arquivo CSS do visualizador externo para o elemento de contêiner do visualizador de nível superior.
* Ao usar a incorporação de tamanho flexível com o método definido por largura e altura da incorporação do visualizador. Consulte o cabeçalho [Incorporação de tamanho flexível com largura e altura definidas](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Desabilite o recurso de pré-carregamento de imagem usando o atributo de configuração `preloadImage` se estiver usando o visualizador em um dos modos de operação listados acima.

Além disso, a imagem de pré-carregamento não é usada, mesmo se habilitada na configuração, se o visualizador estiver incorporado no elemento DOM estiver oculto usando a configuração CSS `display:none` ou desanexado da árvore DOM.
