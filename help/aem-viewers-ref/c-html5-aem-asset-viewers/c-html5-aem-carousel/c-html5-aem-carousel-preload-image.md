---
title: Pré-carregar imagem
description: A imagem de pré-carregamento é uma imagem de visualização de ativo estático que é carregada logo após chamar o método init() e é exibida durante o download das bibliotecas, do ativo e das informações predefinidas do SDK do Visualizador. A finalidade da imagem de pré-carregamento é melhorar visualmente o tempo de carregamento do visualizador e apresentar conteúdo ao usuário rapidamente.
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

A imagem de pré-carregamento é uma imagem de visualização de ativo estático que é carregada logo após chamar o método init() e é exibida durante o download das bibliotecas, do ativo e das informações predefinidas do SDK do Visualizador. A finalidade da imagem de pré-carregamento é melhorar visualmente o tempo de carregamento do visualizador e apresentar conteúdo ao usuário rapidamente.

A imagem de pré-carregamento funciona bem para o método de incorporação do visualizador mais comum, que é a incorporação responsiva com altura irrestrita. Consulte o cabeçalho [Incorporação de design responsivo com altura irrestrita](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

No entanto, o recurso tem determinadas limitações quando outros métodos de incorporação ou opções de configuração específicas são usados. A imagem de pré-carregamento pode não ser renderizada corretamente nos seguintes casos:

* Quando o visualizador é fixado em tamanho e o tamanho é definido usando o atributo de configuração `stagesize` dentro do registro predefinido do visualizador ou, no arquivo CSS do visualizador externo para o elemento do contêiner do visualizador de nível superior.
* Ao usar a incorporação de tamanho flexível com o método de incorporação de largura e altura definido pelo visualizador. Consulte o cabeçalho [Incorporação de tamanho flexível com largura e altura definidas](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Se você usar o visualizador em um dos modos de operação listados acima, desative o recurso de pré-carregamento de imagem usando o atributo de configuração `preloadImage`.

Além disso, a imagem de pré-carregamento não é usada - mesmo se ativada na configuração - se o visualizador estiver incorporado ao elemento DOM estiver oculto usando a configuração `display:none` CSS ou desconectado da árvore DOM.
