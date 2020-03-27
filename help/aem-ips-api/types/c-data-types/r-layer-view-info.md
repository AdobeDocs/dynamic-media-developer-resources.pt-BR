---
description: Propriedades de visualização de camada.
seo-description: Propriedades de visualização de camada.
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
topic: Scene7 Image Production System API
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# LayerViewInfo{#layerviewinfo}

Propriedades de visualização de camada.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| ` *`url`*` | `xsd:string` | URL do servidor de imagens que representa o modelo. Combina `urlModifier` e `urlPostAp- plyModifier` campos. |
| ` *`urlModifier`*` | `xsd:string` | Comandos de protocolo de serviço de imagem a serem aplicados antes da solicitação ou `urlPostApplyModifier` dos comandos. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | Comandos de protocolo de serviço de imagem a serem aplicados após `urlModifier` e solicitar comandos. |

