---
description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-title: Suporte a tecnologia assistiva
solution: Experience Manager
title: Suporte a tecnologia assistiva
topic: Dynamic media
uuid: 0abed8d4-9754-47b1-9de7-cce665de03b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Suporte a tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.

O elemento visualizador de nível superior tem função `region` e `aria-label` atributo definidos por padrão para o nome do visualizador. Você pode controlar o rótulo com o símbolo de `Container.LABEL` localização.

Os botões têm a função `button` e o texto descritivo definidos com o `aria-label` atributo. O valor do `aria-label` atributo é preenchido a partir do valor do símbolo de localização do botão. Quando um botão é desativado, o `aria-disabled` atributo é definido de acordo.

Os componentes do controle deslizante têm a função `slider` com atributos `aria-valuenow`, `aria-valuemin`e `aria-valuemax` para descrever a posição do controle deslizante atual.

As miniaturas têm a função `dialog` com o `aria-label` atributo controlado pelo símbolo de `ThumbnailGridView.LABEL` localização. Miniaturas individuais têm papel `button`. Se uma miniatura for selecionada, o `aria-selected` atributo será definido como `true`.

Os componentes que exibem amostras têm a função `listbox` com o `aria-label` atributo definido para o valor do símbolo de `LABEL` localização desse componente. Amostras individuais têm a função `option` com `aria-setsize` e `aria-posinset` atributos para descrever a posição da amostra no conjunto. Se uma amostra for selecionada, o `aria-selected` atributo será definido como `true`.

listas suspensas são ativadas por botões com `aria-haspopup` atributo adicional definido como `true` e `aria-controls` atributo referenciando o elemento real do painel suspenso. O próprio painel suspenso tem a função `menu` de subelementos com a função `menuitem`. Cada item de menu tem o `aria-label` atributo especificado.

As caixas de diálogo modais têm a função `dialog`. O elemento de cabeçalho da caixa de diálogo é referenciado pelo `aria-labelledby` atributo.
