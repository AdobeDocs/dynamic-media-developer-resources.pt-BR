---
description: Todos os componentes do visualizador oferecem suporte a funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias assistivas, como leitores de tela.
solution: Experience Manager
title: Suporte de tecnologia assistiva
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search,Accessibility
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Suporte de tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador oferecem suporte a funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias assistivas, como leitores de tela.

O elemento do visualizador de nível superior tem o atributo de função `region` e `aria-label` definido por padrão como o nome do visualizador. Você pode controlar o rótulo com o símbolo de localização `Container.LABEL`.

Os botões têm a função `button` e o texto descritivo definido com o atributo `aria-label`. O valor do atributo `aria-label` é preenchido a partir do valor do símbolo de localização do botão. Quando um botão é desativado, o atributo `aria-disabled` é definido adequadamente.

A exibição principal tem a função `application`. Uma breve descrição da exibição principal é fornecida em `aria-roledescription`, com o valor definido pelo símbolo de localização `ROLE_DESCRIPTION` do componente de exibição principal correspondente. As dicas de navegação para usuários de teclado são fornecidas usando `aria-describedby`, o texto da dica de uso vem do símbolo de localização `USAGE_HINT`. Se um ativo tiver um rótulo definido no campo UserData, o atributo `aria-label` será definido com o valor desse rótulo.

Pontos de acesso, regiões e mapas de imagem têm a função `button` e o texto descritivo definidos com o atributo `aria-label`, com o valor do ponto de acesso ou rótulo do mapa de imagem. Quando o usuário coloca um foco em pontos de acesso ou mapas de imagem, as dicas de navegação para usuários de teclado são fornecidas usando `aria-describedby`, com o texto da dica de uso vindo do símbolo de localização `USAGE_HINT`.

As miniaturas têm a função `dialog` com o atributo `aria-label` controlada pelo símbolo de localização `ThumbnailGridView.LABEL`. Miniaturas individuais possuem a função `button`. Se uma miniatura for selecionada, ela obterá o atributo `aria-selected` definido como `true`.

Os componentes que exibem amostras têm a função `listbox` com o atributo `aria-label` definido como o valor do símbolo de localização `LABEL` desse componente. Amostras individuais têm a função `option` com `aria-setsize` e `aria-posinset` atributos para descrever a posição da amostra no conjunto. Se uma amostra for selecionada, ela obterá o atributo `aria-selected` definido como `true`.

As listas suspensas são ativadas por botões com o atributo `aria-haspopup` adicional definido como `true` e o atributo `aria-controls` que faz referência ao elemento real do painel suspenso. O próprio painel suspenso tem a função `menu` com subelementos com a função `menuitem`. Cada item de menu tem o atributo `aria-label` especificado.

A interface de usuário de pesquisa está agrupada no elemento com a função `search`. O campo de entrada de pesquisa tem a função `searchbox` e faz referência ao rótulo informativo controlado pelo símbolo de localização `SearchPanel.INFO_PROMPT` com o atributo `aria-describedby`.

As caixas de diálogo modais têm a função `dialog`. O elemento de cabeçalho da caixa de diálogo é referenciado pelo atributo `aria-labelledby`.
