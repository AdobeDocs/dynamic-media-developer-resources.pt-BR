---
title: Suporte à tecnologia assistiva
description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout,Accessibility
role: Developer,User
exl-id: 0f96939b-0ecc-4d4d-a084-60b023b2a5f2
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Suporte à tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.

O elemento do visualizador de nível superior tem função `region` e `aria-label` por padrão, para o nome do visualizador. Você pode controlar o rótulo com a variável `Container.LABEL` símbolo de localização.

Os botões têm a função `button` e texto descritivo definido com a variável `aria-label` atributo. O valor de `aria-label` é preenchido a partir do valor do símbolo de localização do botão. Quando um botão é desativado, a variável `aria-disabled` é definido de acordo.

A exibição principal tem função `application`. Uma breve descrição da exibição principal é fornecida em `aria-roledescription`, com o valor definido pela variável `ROLE_DESCRIPTION` símbolo de localização do componente de exibição principal correspondente. Dicas de navegação para usuários de teclado são fornecidas usando `aria-describedby`, o texto da dica de uso vem da variável `USAGE_HINT` símbolo de localização. Se um ativo tiver um rótulo definido no campo UserData , a variável `aria-label` é definido com o valor desse rótulo.

Os componentes que exibem amostras têm a função `listbox` com `aria-label` conjunto de atributos para o valor da variável `LABEL` símbolo de localização desse componente. Amostras individuais têm a função `option` com `aria-setsize` e `aria-posinset` atributos para descrever a posição da amostra no conjunto. Se uma amostra for selecionada, ela receberá a variável `aria-selected` conjunto de atributos para `true`.
