---
description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-title: Suporte a tecnologia assistiva
solution: Experience Manager
title: Suporte a tecnologia assistiva
topic: Dynamic media
uuid: 2a6d6e09-a016-407d-b870-92c84fe75ed3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Suporte a tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.

O elemento visualizador de nível superior tem função `region` e `aria-label` atributo definidos por padrão para o nome do visualizador. Você pode controlar o rótulo com o símbolo de `Container.LABEL` localização.

Os botões têm a função `button` e o texto descritivo definidos com o `aria-label` atributo. O valor do `aria-label` atributo é preenchido a partir do valor do símbolo de localização do botão. Quando um botão é desativado, o `aria-disabled` atributo é definido de acordo.

A visualização principal tem papel `application`. Uma breve descrição da visualização principal é fornecida em `aria-roledescription`, com o valor definido pelo símbolo de `ROLE_DESCRIPTION` localização do componente de visualização principal correspondente. As dicas de navegação para os usuários do teclado são fornecidas usando `aria-describedby`, o texto para a dica de uso provém do símbolo de `USAGE_HINT` localização. Se um ativo tiver um rótulo definido no campo UserData, o `aria-label` atributo será definido com o valor desse rótulo.

Os componentes que exibem amostras têm a função `listbox` com o `aria-label` atributo definido para o valor do símbolo de `LABEL` localização desse componente. Amostras individuais têm a função `option` com `aria-setsize` e `aria-posinset` atributos para descrever a posição da amostra no conjunto. Se uma amostra for selecionada, o `aria-selected` atributo será definido como `true`.
