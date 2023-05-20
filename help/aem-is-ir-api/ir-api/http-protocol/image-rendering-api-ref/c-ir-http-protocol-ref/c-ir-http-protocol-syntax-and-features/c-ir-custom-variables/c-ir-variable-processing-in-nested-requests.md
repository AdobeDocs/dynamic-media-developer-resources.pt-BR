---
title: Processamento de variáveis em solicitações aninhadas
description: As referências $var$ podem ocorrer em qualquer lugar dentro das chaves de uma solicitação aninhada de Servidor de imagens ou de Renderização de imagens, inclusive à esquerda de '?' separar o caminho da consulta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Processamento de variáveis em solicitações aninhadas{#variable-processing-in-nested-requests}

As referências $var$ podem ocorrer em qualquer lugar dentro das chaves de uma solicitação aninhada de Servidor de imagens ou de Renderização de imagens, inclusive à esquerda de &#39;?&#39; separar o caminho da consulta.

O servidor substitui essas referências por valores (do url ou do `catalog::Modifier` do catálogo de imagens principal) antes de analisar e processar a solicitação aninhada.

Além disso, todas as `$ *[!DNL var]*=` definições do url e `catalog::Modifier` são encaminhadas para todas as solicitações aninhadas de Servidor de imagens e Renderização de imagens. Isso garante que todas as definições de variável estejam disponíveis para todos os modelos, independentemente do nível de aninhamento.

Independentemente do nível de aninhamento, somente a codificação HTTP de passagem única deve ser aplicada aos valores de variável que devem ser substituídos em qualquer lugar nas solicitações aninhadas de Renderização de imagem ou de Servidor de imagens.
