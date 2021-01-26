---
description: Propriedades de visualização de camada.
seo-description: Propriedades de visualização de camada.
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
topic: Dynamic Media Image Production System API
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 0%

---


# LayerViewInfo{#layerviewinfo}

Propriedades de visualização de camada.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`url`*` | `xsd:string` | URL do servidor de imagens que representa o modelo. Combina os campos `urlModifier` e `urlPostAp- plyModifier`. |
| `*`urlModifier`*` | `xsd:string` | Comandos de protocolo de serviço de imagem a serem aplicados antes dos comandos request ou `urlPostApplyModifier`. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Comandos de protocolo de serviço de imagem a serem aplicados depois de `urlModifier` e comandos de solicitação. |

