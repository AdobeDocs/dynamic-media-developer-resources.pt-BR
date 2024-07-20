---
title: Pré-carregar imagem
description: A imagem pré-carregada é uma imagem de pré-visualização de ativo estático que é carregada logo após chamar o método init() e é exibida enquanto as bibliotecas, o ativo e as informações predefinidas do SDK do Visualizador são baixados. O objetivo do pré-carregamento da imagem é melhorar visualmente o tempo de carregamento do visualizador e apresentar conteúdo ao usuário rapidamente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Pré-carregar imagem{#preload-image}

A imagem pré-carregada é uma imagem de pré-visualização de ativo estático que é carregada logo após chamar o método init() e é exibida enquanto as bibliotecas, o ativo e as informações predefinidas do SDK do Visualizador são baixados. O objetivo do pré-carregamento da imagem é melhorar visualmente o tempo de carregamento do visualizador e apresentar conteúdo ao usuário rapidamente.

O pré-carregamento de imagens funciona bem para o método de incorporação do visualizador mais comum, que é a incorporação responsiva com altura irrestrita. Consulte o cabeçalho [Incorporação responsiva de design com altura irrestrita](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

No entanto, o recurso tem determinadas limitações quando outros métodos de incorporação ou opções de configuração específicas são usados. A imagem pré-carregada pode não ser renderizada corretamente nos seguintes casos:

* Quando o visualizador é fixo em tamanho e o tamanho é definido usando o atributo de configuração `stagesize` dentro do registro de predefinição do visualizador ou no arquivo CSS do visualizador externo para o elemento de contêiner do visualizador de nível superior.
* Ao usar a incorporação de tamanho flexível com o método definido por largura e altura da incorporação do visualizador. Consulte o cabeçalho [Incorporação de tamanho flexível com largura e altura definidas](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Se você usar o visualizador em um dos modos de operação listados acima, desabilite o recurso de pré-carregamento de imagem usando o atributo de configuração `preloadImage`.

Além disso, a imagem de pré-carregamento não é usada, mesmo se habilitada na configuração, se o visualizador estiver incorporado no elemento DOM estiver oculto usando a configuração CSS `display:none` ou desanexado da árvore DOM.
