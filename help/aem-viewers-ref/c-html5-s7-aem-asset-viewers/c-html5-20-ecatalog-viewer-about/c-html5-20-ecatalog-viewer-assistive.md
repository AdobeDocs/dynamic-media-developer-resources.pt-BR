---
title: Suporte de tecnologia assistiva
description: Todos os componentes do visualizador oferecem suporte a funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias assistivas, como leitores de tela.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Suporte de tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador oferecem suporte a funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias assistivas, como leitores de tela.

O elemento do visualizador de nível superior tem função `region` e `aria-label` atributo definido por padrão para o nome do visualizador. É possível controlar o rótulo com a variável `Container.LABEL` símbolo de localização.

Os botões têm a função `button` e texto descritivo definido com a variável `aria-label` atributo. O valor de `aria-label` O atributo é preenchido a partir do valor do símbolo de localização do botão. Quando um botão é desativado, a variável `aria-disabled` atributo é definido de acordo.

A exibição principal tem função `application`. Uma breve descrição da exibição principal é fornecida em `aria-roledescription`, com o valor definido pelo `ROLE_DESCRIPTION` símbolo de localização do componente de exibição principal correspondente. As dicas de navegação para usuários de teclado são fornecidas usando `aria-describedby`, o texto para a dica de uso vem da variável `USAGE_HINT` símbolo de localização. Se um ativo tiver um rótulo definido no campo UserData, a variável `aria-label` atributo é definido com o valor desse rótulo.

Pontos de acesso, regiões e mapas de imagem desempenham a função `button` e texto descritivo definido com `aria-label` atributo, com o valor do ponto de acesso ou rótulo do mapa de imagem. Quando o usuário focaliza pontos de acesso ou mapas de imagem, as dicas de navegação dos usuários de teclado são fornecidas usando `aria-describedby`, com o texto da dica de uso vindo de `USAGE_HINT` símbolo de localização.

As miniaturas têm a função `dialog` com `aria-label` atributo controlado pela `ThumbnailGridView.LABEL` símbolo de localização. Miniaturas individuais têm função `button`. Se uma miniatura for selecionada, ela será `aria-selected` atributo definido como `true`.

Os componentes que exibem amostras têm a função `listbox` com `aria-label` atributo definido para o valor do `LABEL` símbolo de localização desse componente. Amostras individuais têm a função `option` com `aria-setsize` e `aria-posinset` atributos para descrever a posição da amostra no conjunto. Se uma amostra for selecionada, ela obterá a `aria-selected` atributo definido como `true`.

As listas suspensas são ativadas por botões com `aria-haspopup` atributo definido como `true` e a variável `aria-controls` atributo que faz referência ao elemento real do painel suspenso. O próprio painel suspenso tem a função `menu` com subelementos com a função `menuitem`. Cada item de menu tem o `aria-label` atributo especificado.

As caixas de diálogo modais têm a função `dialog`. O elemento de cabeçalho da caixa de diálogo é referenciado pela variável `aria-labelledby` atributo.
