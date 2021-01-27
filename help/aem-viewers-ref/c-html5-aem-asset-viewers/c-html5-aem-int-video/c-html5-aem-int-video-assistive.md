---
description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-title: Suporte a tecnologia assistiva
solution: Experience Manager
title: Suporte a tecnologia assistiva
topic: Dynamic Media
uuid: 0abed8d4-9754-47b1-9de7-cce665de03b4
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---


# Suporte de tecnologia de assistência{#assistive-technology-support}

Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.

O elemento do visualizador de nível superior tem o atributo `region` e `aria-label` definido por padrão para o nome do visualizador. Você pode controlar o rótulo com o símbolo de localização `Container.LABEL`.

Os botões têm a função `button` e o texto descritivo definido com o atributo `aria-label`. O valor do atributo `aria-label` é preenchido a partir do valor do símbolo de localização do botão. Quando um botão é desativado, o atributo `aria-disabled` é definido de acordo.

Os componentes do controle deslizante têm a função `slider` com atributos `aria-valuenow`, `aria-valuemin` e `aria-valuemax` para descrever a posição do controle deslizante atual.

As miniaturas têm a função `dialog` com o atributo `aria-label` controlado pelo símbolo de localização `ThumbnailGridView.LABEL`. As miniaturas individuais têm a função `button`. Se uma miniatura for selecionada, ela terá o atributo `aria-selected` definido como `true`.

Os componentes que exibem amostras têm a função `listbox` com o atributo `aria-label` definido para o valor do símbolo de localização `LABEL` desse componente. Amostras individuais têm a função `option` com os atributos `aria-setsize` e `aria-posinset` para descrever a posição da amostra no conjunto. Se uma amostra for selecionada, o atributo `aria-selected` será definido como `true`.

Listas suspensas são ativadas por botões com o atributo adicional `aria-haspopup` definido como `true` e o atributo `aria-controls` referenciando o elemento real do painel suspenso. O próprio painel suspenso tem a função `menu` com subelementos que têm a função `menuitem`. Cada item de menu tem o atributo `aria-label` especificado.

As caixas de diálogo modais têm a função `dialog`. O elemento de cabeçalho da caixa de diálogo é referenciado pelo atributo `aria-labelledby`.
