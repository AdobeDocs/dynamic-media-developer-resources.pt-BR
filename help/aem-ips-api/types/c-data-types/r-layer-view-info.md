---
description: Propriedades da exibição de camada.
seo-description: Propriedades da exibição de camada.
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
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

