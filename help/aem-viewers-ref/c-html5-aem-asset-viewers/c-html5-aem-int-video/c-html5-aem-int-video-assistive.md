---
title: Suporte de tecnologia assistiva
description: Todos os componentes do visualizador oferecem suporte a funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias assistivas, como leitores de tela.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos,Accessibility
role: Developer,User
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Suporte de tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador oferecem suporte a funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias assistivas, como leitores de tela.

O elemento do visualizador de nível superior tem o atributo de função `region` e `aria-label` definido por padrão como o nome do visualizador. Você pode controlar o rótulo com o símbolo de localização `Container.LABEL`.

Os botões têm a função `button` e o texto descritivo definido com o atributo `aria-label`. O valor do atributo `aria-label` é preenchido a partir do valor do símbolo de localização do botão. Quando um botão é desabilitado, o atributo `aria-disabled` é definido adequadamente.

Os componentes de controle deslizante têm a função `slider` com os atributos `aria-valuenow`, `aria-valuemin` e `aria-valuemax` para descrever a posição atual do controle deslizante.

As miniaturas têm a função `dialog` com o atributo `aria-label` controlada pelo símbolo de localização `ThumbnailGridView.LABEL`. Miniaturas individuais possuem a função `button`. Se uma miniatura for selecionada, ela obterá o atributo `aria-selected` definido como `true`.

Os componentes que exibem amostras têm a função `listbox` com o atributo `aria-label` definido como o valor do símbolo de localização `LABEL` desse componente. Amostras individuais têm a função `option` com `aria-setsize` e `aria-posinset` atributos para descrever a posição da amostra no conjunto. Se uma amostra for selecionada, ela obterá o atributo `aria-selected` definido como `true`.

As listas suspensas são ativadas por botões com o atributo `aria-haspopup` adicional definido como `true` e o atributo `aria-controls` que fazem referência ao elemento real do painel suspenso. O próprio painel suspenso tem a função `menu` com subelementos com a função `menuitem`. Cada item de menu tem o atributo `aria-label` especificado.

As caixas de diálogo modais têm a função `dialog`. O elemento de cabeçalho da caixa de diálogo é referenciado pelo atributo `aria-labelledby`.
