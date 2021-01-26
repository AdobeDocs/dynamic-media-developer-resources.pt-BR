---
description: Referências $var$ que ocorrem em qualquer lugar dentro das chaves de uma solicitação externa incorporada são substituídas por valores de definição de variável correspondentes.
seo-description: Referências $var$ que ocorrem em qualquer lugar dentro das chaves de uma solicitação externa incorporada são substituídas por valores de definição de variável correspondentes.
seo-title: Processamento de variável em solicitações externas incorporadas
solution: Experience Manager
title: Processamento de variável em solicitações externas incorporadas
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b4334a2e-dab1-4458-ab3d-bb79d2c4fdd4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# Processamento de variável em solicitações externas incorporadas{#variable-processing-in-embedded-foreign-requests}

Referências $var$ que ocorrem em qualquer lugar dentro das chaves de uma solicitação externa incorporada são substituídas por valores de definição de variável correspondentes.

Isso permite que solicitações externas incorporadas sejam colocadas em um modelo em um catálogo de imagens.

Normalmente, os valores de variáveis que devem ser substituídos em solicitações estrangeiras devem ser codificados em duplo, já que nenhuma recodificação é aplicada antes que o servidor tente transmitir o url externo final.
