---
title: Processamento de variáveis em solicitações externas inseridas
description: As referências $var$ que ocorrem em qualquer lugar dentro das chaves de uma solicitação externa incorporada são substituídas por valores de definição de variável correspondentes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# Processamento de variáveis em solicitações externas inseridas{#variable-processing-in-embedded-foreign-requests}

Quaisquer referências `$var$` que ocorrem em qualquer lugar dentro das chaves de uma solicitação externa incorporada são substituídas por valores de definição de variável correspondentes.

Permite que solicitações externas incorporadas sejam colocadas em um modelo em um catálogo de imagens.

Os valores de variáveis que devem ser substituídos em solicitações estrangeiras normalmente devem ser codificados duas vezes, porque nenhuma nova codificação é aplicada antes que o servidor tente transmitir o URL externo final.
