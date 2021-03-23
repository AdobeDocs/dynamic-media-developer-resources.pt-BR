---
description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-title: Suporte à tecnologia assistiva
solution: Experience Manager
title: Suporte à tecnologia assistiva
uuid: 525ab400-c022-4f33-a0e3-bafb6019f1a7
feature: Dynamic Media Classic, Visualizadores, SDK/API, Pesquisa de catálogo eletrônico, Acessibilidade
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# Suporte à tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.

O elemento do visualizador de nível superior tem o atributo de função `region` e `aria-label` definido por padrão para o nome do visualizador. Você pode controlar o rótulo com o símbolo de localização `Container.LABEL`.

Os botões têm a função `button` e o texto descritivo definido com o atributo `aria-label`. O valor do atributo `aria-label` é preenchido a partir do valor do símbolo de localização do botão. Quando um botão é desativado, o atributo `aria-disabled` é definido adequadamente.

A exibição principal tem a função `application`. Uma breve descrição da exibição principal é fornecida em `aria-roledescription`, com o valor definido pelo símbolo de localização `ROLE_DESCRIPTION` do componente de exibição principal correspondente. As dicas de navegação para usuários de teclado são fornecidas usando `aria-describedby`, o texto para a dica de uso vem do símbolo de localização `USAGE_HINT`. Se um ativo tiver um rótulo definido no campo UserData , o atributo `aria-label` será definido com o valor desse rótulo.

Os pontos ativos, as regiões e os mapas de imagem têm a função `button` e o texto descritivo definido com o atributo `aria-label`, com o valor do ponto ativo ou rótulo do mapa de imagem. Quando o usuário coloca um foco em pontos ativos ou mapas de imagem, as dicas de navegação para usuários de teclado são fornecidas usando `aria-describedby`, com o texto para a dica de uso proveniente do símbolo de localização `USAGE_HINT`.

As miniaturas têm a função `dialog` com o atributo `aria-label` controlado pelo símbolo de localização `ThumbnailGridView.LABEL`. As miniaturas individuais têm a função `button`. Se uma miniatura for selecionada, ela obterá o atributo `aria-selected` definido como `true`.

Os componentes que exibem amostras têm a função `listbox` com o atributo `aria-label` definido com o valor do símbolo de localização `LABEL` desse componente. Amostras individuais têm a função `option` com atributos `aria-setsize` e `aria-posinset` para descrever a posição da amostra no conjunto. Se uma amostra for selecionada, ele obterá o atributo `aria-selected` definido como `true`.

As listas suspensas são ativadas por botões com o atributo `aria-haspopup` adicional definido como `true` e o atributo `aria-controls` referenciando o elemento real do painel suspenso. O próprio painel suspenso tem a função `menu` com subelementos com a função `menuitem`. Cada item de menu tem o atributo `aria-label` especificado.

A interface do usuário de pesquisa é agrupada no elemento com a função `search`. O campo de entrada de pesquisa tem a função `searchbox` e faz referência ao rótulo informativo controlado pelo símbolo de localização `SearchPanel.INFO_PROMPT` com o atributo `aria-describedby`.

As caixas de diálogo modais têm a função `dialog`. O elemento de cabeçalho da caixa de diálogo é referenciado pelo atributo `aria-labelledby`.
