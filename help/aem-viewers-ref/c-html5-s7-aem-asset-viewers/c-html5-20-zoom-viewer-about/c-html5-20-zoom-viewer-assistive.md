---
title: Suporte de tecnologia assistiva
description: Todos os componentes do visualizador oferecem suporte a funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias assistivas, como leitores de tela.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom,Accessibility
role: Developer,User
exl-id: ef2cf58a-bdf0-4136-8d91-692c899cfef7
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Suporte de tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador oferecem suporte a funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias assistivas, como leitores de tela.

O elemento do visualizador de nível superior tem o atributo de função `region` e `aria-label` definido por padrão como o nome do visualizador. Você pode controlar o rótulo com o símbolo de localização `Container.LABEL`.

Os botões têm a função `button` e o texto descritivo definido com o atributo `aria-label`. O valor do atributo `aria-label` é preenchido a partir do valor do símbolo de localização do botão. Quando um botão é desabilitado, o atributo `aria-disabled` é definido adequadamente.

A exibição principal tem a função `application`. Uma breve descrição da exibição principal é fornecida em `aria-roledescription`, com o valor definido pelo símbolo de localização `ROLE_DESCRIPTION` do componente de exibição principal correspondente. As dicas de navegação para usuários de teclado são fornecidas usando `aria-describedby`, o texto da dica de uso vem do símbolo de localização `USAGE_HINT`. Se um ativo tiver um rótulo definido no campo UserData, o atributo `aria-label` será definido com o valor desse rótulo.

Os componentes que exibem amostras têm a função `listbox` com o atributo `aria-label` definido como o valor do símbolo de localização `LABEL` desse componente. Amostras individuais têm a função `option` com `aria-setsize` e `aria-posinset` atributos para descrever a posição da amostra no conjunto. Se uma amostra for selecionada, ela obterá o atributo `aria-selected` definido como `true`.
