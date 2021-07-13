---
description: As referências $var$ que ocorrem em qualquer lugar nas chaves de uma solicitação externa incorporada são substituídas por valores de definição de variável correspondentes.
solution: Experience Manager
title: Processamento de variável em solicitações externas incorporadas
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Processamento de variável em solicitações externas incorporadas{#variable-processing-in-embedded-foreign-requests}

As referências $var$ que ocorrem em qualquer lugar nas chaves de uma solicitação externa incorporada são substituídas por valores de definição de variável correspondentes.

Isso permite que solicitações externas incorporadas sejam colocadas em um modelo em um catálogo de imagem.

Os valores de variáveis que devem ser substituídos em solicitações estrangeiras normalmente devem ser codificados duas vezes, já que nenhuma recodificação é aplicada antes que o servidor tente transmitir o url externo final.
