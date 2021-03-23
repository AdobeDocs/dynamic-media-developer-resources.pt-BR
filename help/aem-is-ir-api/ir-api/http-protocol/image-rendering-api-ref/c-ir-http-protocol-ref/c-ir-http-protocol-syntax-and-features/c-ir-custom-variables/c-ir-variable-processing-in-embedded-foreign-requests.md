---
description: As referências $var$ que ocorrem em qualquer lugar nas chaves de uma solicitação externa incorporada são substituídas por valores de definição de variável correspondentes.
seo-description: As referências $var$ que ocorrem em qualquer lugar nas chaves de uma solicitação externa incorporada são substituídas por valores de definição de variável correspondentes.
seo-title: Processamento de variável em solicitações externas incorporadas
solution: Experience Manager
title: Processamento de variável em solicitações externas incorporadas
uuid: b4334a2e-dab1-4458-ab3d-bb79d2c4fdd4
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# Processamento de variável em solicitações externas incorporadas{#variable-processing-in-embedded-foreign-requests}

As referências $var$ que ocorrem em qualquer lugar nas chaves de uma solicitação externa incorporada são substituídas por valores de definição de variável correspondentes.

Isso permite que solicitações externas incorporadas sejam colocadas em um modelo em um catálogo de imagem.

Os valores de variáveis que devem ser substituídos em solicitações estrangeiras normalmente devem ser codificados duas vezes, já que nenhuma recodificação é aplicada antes que o servidor tente transmitir o url externo final.
