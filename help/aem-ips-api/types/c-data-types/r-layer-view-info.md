---
description: Propriedades da exibição de camada.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 0%

---

# LayerViewInfo{#layerviewinfo}

Propriedades da exibição de camada.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`url`*` | `xsd:string` | URL do servidor de imagem que representa o modelo. Combina os campos `urlModifier` e `urlPostAp- plyModifier`. |
| `*`urlModifier`*` | `xsd:string` | Comandos de protocolo de veiculação de imagens a serem aplicados antes dos comandos de solicitação ou `urlPostApplyModifier`. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Comandos de protocolo de veiculação de imagens a serem aplicados depois de `urlModifier` e solicitar comandos. |
