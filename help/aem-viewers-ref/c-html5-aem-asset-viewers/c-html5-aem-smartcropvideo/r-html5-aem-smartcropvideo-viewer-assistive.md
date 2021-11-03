---
description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
solution: Experience Manager
title: Suporte à tecnologia assistiva
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video,Accessibility
role: Developer,User
exl-id: e0652730-60ee-41db-890b-e223b279e47d
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Suporte à tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.

O elemento do visualizador de nível superior tem função `region` e `aria-label` por padrão, para o nome do visualizador. Você pode controlar o rótulo com a variável `Container.LABEL` símbolo de localização.

Os botões têm a função `button` e texto descritivo definido com `aria-label` atributo. O valor de `aria-label` é preenchido a partir do valor do símbolo de localização do botão. Quando um botão é desativado, `aria-disabled` é definido de acordo.

Os componentes do controle deslizante têm a função `slider` com atributos `aria-valuenow`, `aria-valuemin`e `aria-valuemax` para descrever a posição do controle deslizante atual.

As listas suspensas são ativadas por botões com outros `aria-haspopup` conjunto de atributos para `true` e `aria-controls` que faz referência ao elemento real do painel suspenso. O próprio painel suspenso tem a função `menu` com subelementos com a função `menuitem`. Cada item de menu tem a variável `aria-label` atributo especificado.

As caixas de diálogo modais têm a função `dialog`. O elemento de cabeçalho da caixa de diálogo é referenciado pela variável `aria-labelledby` atributo.
