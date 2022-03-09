---
description: Propriedades da exibição de camada.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 0%

---

# LayerViewInfo{#layerviewinfo}

Propriedades da exibição de camada.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| url | `xsd:string` | URL do servidor de imagem que representa o modelo. Combinações `urlModifier` e `urlPostAp- plyModifier` campos. |
| urlModifier | `xsd:string` | Comandos de protocolo de veiculação de imagens a serem aplicados antes da solicitação ou `urlPostApplyModifier` comandos. |
| urlPostApplyModifier | `xsd:string` | Comandos do protocolo de veiculação de imagens a serem aplicados depois `urlModifier` e solicitar comandos. |
