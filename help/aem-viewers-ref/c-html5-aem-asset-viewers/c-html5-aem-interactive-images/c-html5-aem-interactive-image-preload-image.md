---
description: A imagem de pré-carregamento é uma imagem de pré-visualização de ativo estático que é carregada logo após chamar o método init() e é exibida enquanto as bibliotecas do SDK do visualizador, as informações de ativo e predefinidas são baixadas. A finalidade da imagem de pré-carregamento é melhorar visualmente o tempo de carregamento do visualizador e apresentar conteúdo ao usuário rapidamente.
seo-description: A imagem de pré-carregamento é uma imagem de pré-visualização de ativo estático que é carregada logo após chamar o método init() e é exibida enquanto as bibliotecas do SDK do visualizador, as informações de ativo e predefinidas são baixadas. A finalidade da imagem de pré-carregamento é melhorar visualmente o tempo de carregamento do visualizador e apresentar conteúdo ao usuário rapidamente.
seo-title: Pré-carregar imagem
solution: Experience Manager
title: Pré-carregar imagem
topic: Dynamic media
uuid: cb5db16d-b496-40e4-b8ef-5573c42d2850
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Pré-carregar imagem{#preload-image}

A imagem de pré-carregamento é uma imagem de pré-visualização de ativo estático que é carregada logo após chamar o método init() e é exibida enquanto as bibliotecas do SDK do visualizador, as informações de ativo e predefinidas são baixadas. A finalidade da imagem de pré-carregamento é melhorar visualmente o tempo de carregamento do visualizador e apresentar conteúdo ao usuário rapidamente.

A imagem de pré-carregamento funciona bem para o método de incorporação mais comum do visualizador, que é a incorporação responsiva com altura irrestrita. Consulte o cabeçalho [Incorporação de design responsivo com altura](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)irrestrita.

O recurso, no entanto, tem certas limitações quando outros métodos de incorporação ou opções de configuração específicas são usados. A imagem de pré-carregamento pode falhar na renderização correta nos seguintes casos:

* Quando o tamanho do visualizador é fixo e o tamanho é definido usando o atributo de `stagesize` configuração dentro do registro predefinido do visualizador ou no arquivo CSS do visualizador externo para o elemento de container do visualizador de nível superior.
* Quando a incorporação de tamanho flexível com o método de incorporação do visualizador definido por largura e altura é usada. Consulte o cabeçalho Incorporação de tamanho [flexível com largura e altura definidas](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Talvez seja necessário desativar o recurso de pré-carregamento de imagem usando o atributo de `preloadImage` configuração se você estiver usando o visualizador em um dos modos de operação listados acima.

Além disso, a imagem de pré-carregamento não é usada - mesmo se ativada na configuração - se o visualizador estiver incorporado ao elemento DOM estiver oculto usando a configuração `display:none` CSS ou desconectado da árvore DOM.
