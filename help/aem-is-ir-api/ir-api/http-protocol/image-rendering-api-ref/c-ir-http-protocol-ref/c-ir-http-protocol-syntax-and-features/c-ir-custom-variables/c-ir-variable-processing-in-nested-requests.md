---
title: Processamento de variáveis em solicitações aninhadas
description: As referências $var$ podem ocorrer em qualquer lugar dentro das chaves de uma solicitação aninhada de Servidor de imagens ou de Renderização de imagens, inclusive à esquerda do caractere '?' que separa o caminho da consulta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
TQID: 'https://experienceleague.adobe.com/m7BlSGU8gSozgp8fvNcWuMz5uvpUrfMi4fV5yCYH5bs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 0%

---

# Processamento de variáveis em solicitações aninhadas{#variable-processing-in-nested-requests}

As referências $var$ podem ocorrer em qualquer lugar dentro das chaves de uma solicitação aninhada de Servidor de imagens ou de Renderização de imagens, inclusive à esquerda do caractere &#39;?&#39; que separa o caminho da consulta.

O servidor substitui essas referências por valores (da url ou do `catalog::Modifier` do catálogo de imagens principal) antes de analisar e processar a solicitação aninhada.

Além disso, todas as definições `$ *[!DNL var]*=` da URL e `catalog::Modifier` são encaminhadas para todas as solicitações aninhadas de Servidor de Imagens e de Renderização de Imagens. Isso garante que todas as definições de variável estejam disponíveis para todos os modelos, independentemente do nível de aninhamento.

Independentemente do nível de aninhamento, somente a codificação HTTP de passagem única deve ser aplicada aos valores de variável que devem ser substituídos em qualquer lugar nas solicitações aninhadas de Renderização de imagem ou de Servidor de imagens.
