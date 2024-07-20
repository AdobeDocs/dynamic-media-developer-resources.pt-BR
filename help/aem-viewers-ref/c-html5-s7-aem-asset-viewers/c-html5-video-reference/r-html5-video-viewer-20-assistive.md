---
title: Suporte de tecnologia assistiva
description: Todos os componentes do visualizador oferecem suporte a funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias assistivas, como leitores de tela.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video,Accessibility
role: Developer,User
exl-id: e0652730-60ee-41db-890b-e223b279e47d
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Suporte de tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador oferecem suporte a funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias assistivas, como leitores de tela.

O elemento do visualizador de nível superior tem o atributo de função `region` e `aria-label` definido por padrão como o nome do visualizador. Você pode controlar o rótulo com o símbolo de localização `Container.LABEL`.

Os botões têm a função `button` e o texto descritivo definido com o atributo `aria-label`. O valor do atributo `aria-label` é preenchido a partir do valor do símbolo de localização do botão. Quando um botão é desabilitado, o atributo `aria-disabled` é definido adequadamente.

Os componentes de controle deslizante têm a função `slider` com os atributos `aria-valuenow`, `aria-valuemin` e `aria-valuemax` para descrever a posição atual do controle deslizante.

As listas suspensas são ativadas por botões com o atributo `aria-haspopup` adicional definido como `true` e o atributo `aria-controls` que fazem referência ao elemento real do painel suspenso. O próprio painel suspenso tem a função `menu` com subelementos com a função `menuitem`. Cada item de menu tem o atributo `aria-label` especificado.

As caixas de diálogo modais têm a função `dialog`. O elemento de cabeçalho da caixa de diálogo é referenciado pelo atributo `aria-labelledby`.
