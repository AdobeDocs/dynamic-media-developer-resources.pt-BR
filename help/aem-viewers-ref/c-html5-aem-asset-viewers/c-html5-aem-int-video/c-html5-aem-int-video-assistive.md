---
description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
solution: Experience Manager
title: Suporte à tecnologia assistiva
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos,Acessibilidade
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---


# Suporte à tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.

O elemento do visualizador de nível superior tem o atributo de função `region` e `aria-label` definido por padrão para o nome do visualizador. Você pode controlar o rótulo com o símbolo de localização `Container.LABEL`.

Os botões têm a função `button` e o texto descritivo definido com o atributo `aria-label`. O valor do atributo `aria-label` é preenchido a partir do valor do símbolo de localização do botão. Quando um botão é desativado, o atributo `aria-disabled` é definido adequadamente.

Os componentes do controle deslizante têm a função `slider` com atributos `aria-valuenow`, `aria-valuemin` e `aria-valuemax` para descrever a posição do controle deslizante atual.

As miniaturas têm a função `dialog` com o atributo `aria-label` controlado pelo símbolo de localização `ThumbnailGridView.LABEL`. As miniaturas individuais têm a função `button`. Se uma miniatura for selecionada, ela obterá o atributo `aria-selected` definido como `true`.

Os componentes que exibem amostras têm a função `listbox` com o atributo `aria-label` definido com o valor do símbolo de localização `LABEL` desse componente. Amostras individuais têm a função `option` com atributos `aria-setsize` e `aria-posinset` para descrever a posição da amostra no conjunto. Se uma amostra for selecionada, ele obterá o atributo `aria-selected` definido como `true`.

As listas suspensas são ativadas por botões com atributo `aria-haspopup` adicional definido como `true` e atributo `aria-controls` referenciando o elemento real do painel suspenso. O próprio painel suspenso tem a função `menu` com subelementos com a função `menuitem`. Cada item de menu tem o atributo `aria-label` especificado.

As caixas de diálogo modais têm a função `dialog`. O elemento de cabeçalho da caixa de diálogo é referenciado pelo atributo `aria-labelledby`.
