---
title: Pré-carregar imagem
description: A imagem pré-carregada é uma imagem de pré-visualização de ativo estático que é carregada logo após chamar o método init() e é exibida enquanto as bibliotecas, os ativos e as informações predefinidas do SDK do Viewer são baixados. O objetivo do pré-carregamento da imagem é melhorar visualmente o tempo de carregamento do visualizador e apresentar conteúdo ao usuário rapidamente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
TQID: 'https://experienceleague.adobe.com/0Gm-U-1l0osVADyWyLCH4rJRUCuRHgUJ8XNsbDNpkgc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 266
ht-degree: 0%

---

# Pré-carregar imagem{#preload-image}

A imagem pré-carregada é uma imagem de pré-visualização de ativo estático que é carregada logo após chamar o método init() e é exibida enquanto as bibliotecas, os ativos e as informações predefinidas do SDK do Viewer são baixados. O objetivo do pré-carregamento da imagem é melhorar visualmente o tempo de carregamento do visualizador e apresentar conteúdo ao usuário rapidamente.

O pré-carregamento de imagens funciona bem para o método de incorporação do visualizador mais comum, que é a incorporação responsiva com altura irrestrita. Consulte o cabeçalho [Incorporação responsiva de design com altura irrestrita](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

No entanto, o recurso tem determinadas limitações quando outros métodos de incorporação ou opções de configuração específicas são usados. A imagem pré-carregada pode não ser renderizada corretamente nos seguintes casos:

* Quando o visualizador é fixo em tamanho e o tamanho é definido usando o atributo de configuração `stagesize` dentro do registro de predefinição do visualizador ou no arquivo CSS do visualizador externo para o elemento de contêiner do visualizador de nível superior.
* Ao usar a incorporação de tamanho flexível com o método definido por largura e altura da incorporação do visualizador. Consulte o cabeçalho [Incorporação de tamanho flexível com largura e altura definidas](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Se você usar o visualizador em um dos modos de operação listados acima, desabilite o recurso de pré-carregamento de imagem usando o atributo de configuração `preloadImage`.

Além disso, a imagem de pré-carregamento não é usada, mesmo se habilitada na configuração, se o visualizador estiver incorporado no elemento DOM estiver oculto usando a configuração CSS `display:none` ou desanexado da árvore DOM.
