---
title: Suporte de tecnologia assistiva
description: Todos os componentes do visualizador oferecem suporte a funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias assistivas, como leitores de tela.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images,Accessibility
role: Developer,User
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Suporte de tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador oferecem suporte a funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias assistivas, como leitores de tela.

O elemento do visualizador de nível superior tem o atributo de função `region` e `aria-label` definido por padrão como o nome do visualizador. Você pode controlar o rótulo com o símbolo de localização `Container.LABEL`.

A exibição principal tem a função `application`. Uma breve descrição da exibição principal é fornecida em `aria-roledescription`, com o valor definido pelo símbolo de localização `ROLE_DESCRIPTION` do componente de exibição principal correspondente. As dicas de navegação para usuários de teclado são fornecidas usando `aria-describedby`, o texto da dica de uso vem do símbolo de localização `USAGE_HINT`. Se um ativo tiver um rótulo definido no campo UserData, o atributo `aria-label` será definido com o valor desse rótulo.

Pontos de acesso, regiões e mapas de imagem têm a função `button` e o texto descritivo definidos com o atributo `aria-label`, com o valor do ponto de acesso ou rótulo do mapa de imagem. Quando o usuário coloca um foco em pontos de acesso ou mapas de imagem, as dicas de navegação para usuários de teclado são fornecidas usando `aria-describedby`, com o texto da dica de uso vindo do símbolo de localização `USAGE_HINT`.
