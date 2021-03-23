---
description: As referências $var$ podem ocorrer em qualquer lugar dentro das chaves de uma solicitação aninhada de Exibição de imagem ou Renderização de imagem, incluindo à esquerda de '?' separando o caminho da query.
seo-description: As referências $var$ podem ocorrer em qualquer lugar dentro das chaves de uma solicitação aninhada de Exibição de imagem ou Renderização de imagem, incluindo à esquerda de '?' separando o caminho da query.
seo-title: Processamento de variável em solicitações aninhadas
solution: Experience Manager
title: Processamento de variável em solicitações aninhadas
uuid: 2f3fefac-d45e-4c53-854f-1fe16d0cedd9
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# Processamento de variável em solicitações aninhadas{#variable-processing-in-nested-requests}

As referências $var$ podem ocorrer em qualquer lugar dentro das chaves de uma solicitação aninhada de Exibição de imagem ou Renderização de imagem, incluindo à esquerda de &#39;?&#39; separando o caminho da query.

O servidor substitui essas referências por valores (do url ou de `catalog::Modifier` do catálogo de imagens principal) antes de analisar e processar a solicitação aninhada.

Além disso, todas as definições `$ *[!DNL var]*=` do url e `catalog::Modifier` são encaminhadas para todas as solicitações aninhadas de Exibição de imagem e Renderização de imagem. Isso garante que todas as definições de variável estejam disponíveis para todos os modelos, independentemente do nível de aninhamento.

Independentemente do nível de aninhamento, somente a codificação HTTP de passagem única deve ser aplicada a valores variáveis que devem ser substituídos em qualquer lugar nas solicitações aninhadas de Renderização de imagem ou Exibição de imagem.
