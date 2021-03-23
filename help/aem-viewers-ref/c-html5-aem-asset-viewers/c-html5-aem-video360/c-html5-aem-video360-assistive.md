---
description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-description: Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.
seo-title: Suporte à tecnologia assistiva
solution: Experience Manager
title: Suporte à tecnologia assistiva
uuid: 52f5dad9-7309-4385-99bc-79d02d3ba2d9
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo 360 VR,Acessibilidade
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# Suporte à tecnologia assistiva{#assistive-technology-support}

Todos os componentes do visualizador suportam funções e atributos ARIA (Accessible Rich Internet Applications) para melhorar a integração com tecnologias de assistência, como leitores de tela.

O elemento do visualizador de nível superior tem o atributo de função `region` e `aria-label` definido por padrão para o nome do visualizador. Você pode controlar o rótulo com o símbolo de localização `Container.LABEL`.

Os botões têm a função `button` e o texto descritivo definido com o atributo `aria-label`. O valor do atributo `aria-label` é preenchido a partir do valor do símbolo de localização do botão. Quando um botão é desativado, o atributo `aria-disabled` é definido adequadamente.

Os componentes do controle deslizante têm a função `slider` com atributos `aria-valuenow`, `aria-valuemin` e `aria-valuemax` para descrever a posição do controle deslizante atual.

As listas suspensas são ativadas por botões com atributo `aria-haspopup` adicional definido como `true` e atributo `aria-controls` referenciando o elemento real do painel suspenso. O próprio painel suspenso tem a função `menu` com subelementos com a função `menuitem`. Cada item de menu tem o atributo `aria-label` especificado.

As caixas de diálogo modais têm a função `dialog`. O elemento de cabeçalho da caixa de diálogo é referenciado pelo atributo `aria-labelledby`.
