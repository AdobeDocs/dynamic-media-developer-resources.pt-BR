---
description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-title: Suporte a tecnologia assistiva
solution: Experience Manager
title: Suporte a tecnologia assistiva
topic: Dynamic media
uuid: 525ab400-c022-4f33-a0e3-bafb6019f1a7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Suporte a tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.

O elemento visualizador de nível superior tem função `region` e `aria-label` atributo definidos por padrão para o nome do visualizador. Você pode controlar o rótulo com o símbolo de `Container.LABEL` localização.

Os botões têm a função `button` e o texto descritivo definidos com o `aria-label` atributo. O valor do `aria-label` atributo é preenchido a partir do valor do símbolo de localização do botão. Quando um botão é desativado, o `aria-disabled` atributo é definido de acordo.

A visualização principal tem papel `application`. Uma breve descrição da visualização principal é fornecida em `aria-roledescription`, com o valor definido pelo símbolo de `ROLE_DESCRIPTION` localização do componente de visualização principal correspondente. As dicas de navegação para os usuários do teclado são fornecidas usando `aria-describedby`, o texto para a dica de uso provém do símbolo de `USAGE_HINT` localização. Se um ativo tiver um rótulo definido no campo UserData, o `aria-label` atributo será definido com o valor desse rótulo.

Pontos ativos, regiões e mapas de imagem têm a função `button` e o texto descritivo definidos com `aria-label` atributo, com o valor do ponto ativo ou rótulo do mapa de imagem. Quando o usuário coloca o foco em pontos de acesso ou mapas de imagem, as dicas de navegação para usuários do teclado são fornecidas usando `aria-describedby`, com o texto da dica de uso proveniente do símbolo de `USAGE_HINT` localização.

As miniaturas têm a função `dialog` com o `aria-label` atributo controlado pelo símbolo de `ThumbnailGridView.LABEL` localização. Miniaturas individuais têm papel `button`. Se uma miniatura for selecionada, o `aria-selected` atributo será definido como `true`.

Os componentes que exibem amostras têm a função `listbox` com o `aria-label` atributo definido para o valor do símbolo de `LABEL` localização desse componente. Amostras individuais têm a função `option` com `aria-setsize` e `aria-posinset` atributos para descrever a posição da amostra no conjunto. Se uma amostra for selecionada, o `aria-selected` atributo será definido como `true`.

listas suspensas são ativadas por botões com um `aria-haspopup` atributo adicional definido como `true` e o `aria-controls` atributo que faz referência ao elemento do painel suspenso. O próprio painel suspenso tem a função `menu` de subelementos com a função `menuitem`. Cada item de menu tem o `aria-label` atributo especificado.

A interface do usuário de pesquisa é agrupada no elemento com a função `search`. O campo de entrada de pesquisa tem a função `searchbox` e faz referência ao rótulo informativo controlado pelo símbolo de `SearchPanel.INFO_PROMPT` localização com `aria-describedby` atributo.

As caixas de diálogo modais têm a função `dialog`. O elemento de cabeçalho da caixa de diálogo é referenciado pelo `aria-labelledby` atributo.
