---
description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-title: Suporte a tecnologia assistiva
solution: Experience Manager
title: Suporte a tecnologia assistiva
topic: Dynamic Media
uuid: 9de323c9-d383-41e9-ae44-06600f44a85e
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---


# Suporte de tecnologia de assistência{#assistive-technology-support}

Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.

O elemento do visualizador de nível superior tem o atributo `region` e `aria-label` definido por padrão para o nome do visualizador. Você pode controlar o rótulo com o símbolo de localização `Container.LABEL`.

A visualização principal tem a função `application`. Uma breve descrição da visualização principal é fornecida em `aria-roledescription`, com o valor definido pelo símbolo de localização `ROLE_DESCRIPTION` do componente de visualização principal correspondente. As dicas de navegação para usuários de teclado são fornecidas usando `aria-describedby`, o texto para a dica de uso vem do símbolo de localização `USAGE_HINT`. Se um ativo tiver um rótulo definido no campo UserData, o atributo `aria-label` será definido com o valor desse rótulo.

Os componentes que exibem amostras têm a função `listbox` com o atributo `aria-label` definido para o valor do símbolo de localização `LABEL` desse componente. Amostras individuais têm a função `option` com os atributos `aria-setsize` e `aria-posinset` para descrever a posição da amostra no conjunto. Se uma amostra for selecionada, o atributo `aria-selected` será definido como `true`.
