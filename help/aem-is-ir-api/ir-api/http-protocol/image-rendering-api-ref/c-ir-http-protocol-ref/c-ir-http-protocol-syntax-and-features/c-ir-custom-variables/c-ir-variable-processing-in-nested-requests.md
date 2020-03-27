---
description: As referências $var$ podem ocorrer em qualquer lugar dentro das chaves de uma solicitação aninhada de disponibilização de imagem ou renderização de imagem, incluindo à esquerda de '?' separando o caminho do query.
seo-description: As referências $var$ podem ocorrer em qualquer lugar dentro das chaves de uma solicitação aninhada de disponibilização de imagem ou renderização de imagem, incluindo à esquerda de '?' separando o caminho do query.
seo-title: Processamento de variável em solicitações aninhadas
solution: Experience Manager
title: Processamento de variável em solicitações aninhadas
topic: Scene7 Image Serving - Image Rendering API
uuid: 2f3fefac-d45e-4c53-854f-1fe16d0cedd9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Processamento de variável em solicitações aninhadas{#variable-processing-in-nested-requests}

As referências $var$ podem ocorrer em qualquer lugar dentro das chaves de uma solicitação aninhada de disponibilização de imagem ou renderização de imagem, incluindo à esquerda de &#39;?&#39; separando o caminho do query.

O servidor substitui essas referências por valores (do url ou do catálogo de imagens principal) antes de analisar e processar a solicitação aninhada. `catalog::Modifier`

Além disso, todas as `$ *[!DNL var]*=` definições do url e `catalog::Modifier` são encaminhadas para todas as solicitações aninhadas de Serviço de imagem e Renderização de imagem. Isso garante que todas as definições de variáveis estejam disponíveis para todos os modelos, independentemente do nível de aninhamento.

Independentemente do nível de aninhamento, somente a codificação HTTP de passagem única deve ser aplicada a valores variáveis que devem ser substituídos em qualquer lugar nas solicitações aninhadas de Renderização de imagem ou de Serviço de imagem.
