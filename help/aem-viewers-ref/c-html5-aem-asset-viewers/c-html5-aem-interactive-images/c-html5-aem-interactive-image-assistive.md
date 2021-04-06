---
description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
solution: Experience Manager
title: Suporte à tecnologia assistiva
feature: Dynamic Media Classic, Visualizadores, SDK/API, Imagens interativas, Acessibilidade
role: Desenvolvedor,Profissional de negócios
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# Suporte à tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.

O elemento do visualizador de nível superior tem o atributo de função `region` e `aria-label` definido por padrão para o nome do visualizador. Você pode controlar o rótulo com o símbolo de localização `Container.LABEL`.

A exibição principal tem a função `application`. Uma breve descrição da exibição principal é fornecida em `aria-roledescription`, com o valor definido pelo símbolo de localização `ROLE_DESCRIPTION` do componente de exibição principal correspondente. As dicas de navegação para usuários de teclado são fornecidas usando `aria-describedby`, o texto para a dica de uso vem do símbolo de localização `USAGE_HINT`. Se um ativo tiver um rótulo definido no campo UserData , o atributo `aria-label` será definido com o valor desse rótulo.

Os pontos ativos, as regiões e os mapas de imagem têm a função `button` e o texto descritivo definido com o atributo `aria-label`, com o valor do ponto ativo ou rótulo do mapa de imagem. Quando o usuário coloca um foco em pontos ativos ou mapas de imagem, as dicas de navegação para usuários de teclado são fornecidas usando `aria-describedby`, com o texto para a dica de uso proveniente do símbolo de localização `USAGE_HINT`.
