---
description: As referências $var$ que ocorrem em qualquer lugar nas chaves de uma solicitação externa incorporada são substituídas por valores de definição de variável correspondentes.
solution: Experience Manager
title: Processamento de variável em solicitações externas incorporadas
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# Processamento de variável em solicitações externas incorporadas{#variable-processing-in-embedded-foreign-requests}

As referências $var$ que ocorrem em qualquer lugar nas chaves de uma solicitação externa incorporada são substituídas por valores de definição de variável correspondentes.

Isso permite que solicitações externas incorporadas sejam colocadas em um modelo em um catálogo de imagem.

Os valores de variáveis que devem ser substituídos em solicitações estrangeiras normalmente devem ser codificados duas vezes, já que nenhuma recodificação é aplicada antes que o servidor tente transmitir o url externo final.
