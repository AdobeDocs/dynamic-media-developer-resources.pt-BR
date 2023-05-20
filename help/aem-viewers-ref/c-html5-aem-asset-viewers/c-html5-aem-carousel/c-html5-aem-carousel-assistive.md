---
title: Suporte de tecnologia assistiva
description: Todos os componentes do visualizador oferecem suporte a funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias assistivas, como leitores de tela.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners,Accessibility
role: Developer,User
exl-id: 3ed943e8-4695-4561-9be0-1b6ed30294f8
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# Suporte de tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador oferecem suporte a funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias assistivas, como leitores de tela.

O elemento do visualizador de nível superior tem função `region` e `aria-label` atributo definido por padrão para o nome do visualizador. É possível controlar o rótulo com a variável `Container.LABEL` símbolo de localização.

Os botões têm a função `button` e texto descritivo definido com `aria-label` atributo. O valor de `aria-label` O atributo é preenchido a partir do valor do símbolo de localização do botão. Quando um botão está desativado, `aria-disabled` atributo é definido de acordo.

Os botões que permitem navegar pelos slides do carrossel têm rótulos que são atualizados em tempo de execução, dependendo do slide selecionado no momento. O modelo para o rótulo desses botões é definido com `CAROUSELVIEWER_TOOLTIP_GOTO` símbolo de localização.

A exibição principal tem função `application`. Uma breve descrição da exibição principal é fornecida em `aria-roledescription`, com o valor definido pelo `ROLE_DESCRIPTION` símbolo de localização do componente de exibição principal correspondente. As dicas de navegação para usuários de teclado são fornecidas usando `aria-describedby`, o texto para a dica de uso vem da variável `USAGE_HINT` símbolo de localização. Se um ativo tiver um rótulo definido no campo UserData, a variável `aria-label` atributo é definido com o valor desse rótulo.

Pontos de acesso, regiões e mapas de imagem desempenham a função `button` e texto descritivo definido com `aria-label` atributo, com o valor do ponto de acesso ou rótulo do mapa de imagem. Quando o usuário focaliza pontos de acesso ou mapas de imagem, as dicas de navegação dos usuários de teclado são fornecidas usando `aria-describedby`, com o texto da dica de uso vindo de `USAGE_HINT` símbolo de localização.
