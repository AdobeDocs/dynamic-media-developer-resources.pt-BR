---
description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-title: Suporte a tecnologia assistiva
solution: Experience Manager
title: Suporte a tecnologia assistiva
topic: Dynamic media
uuid: 5f6a021f-750c-40e1-be01-86c3750fd25f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Suporte a tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.

O elemento visualizador de nível superior tem função `region` e `aria-label` atributo definidos por padrão para o nome do visualizador. Você pode controlar o rótulo com o símbolo de `Container.LABEL` localização.

A visualização principal tem papel `application`. Uma breve descrição da visualização principal é fornecida em `aria-roledescription`, com o valor definido pelo símbolo de `ROLE_DESCRIPTION` localização do componente de visualização principal correspondente. As dicas de navegação para os usuários do teclado são fornecidas usando `aria-describedby`, o texto para a dica de uso provém do símbolo de `USAGE_HINT` localização. Se um ativo tiver um rótulo definido no campo UserData, o `aria-label` atributo será definido com o valor desse rótulo.

Pontos ativos, regiões e mapas de imagem têm a função `button` e o texto descritivo definidos com `aria-label` atributo, com o valor do ponto ativo ou rótulo do mapa de imagem. Quando o usuário coloca o foco em pontos de acesso ou mapas de imagem, as dicas de navegação para usuários do teclado são fornecidas usando `aria-describedby`, com o texto da dica de uso proveniente do símbolo de `USAGE_HINT` localização.
