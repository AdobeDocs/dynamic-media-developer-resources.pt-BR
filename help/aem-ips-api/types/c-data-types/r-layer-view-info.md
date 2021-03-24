---
description: Propriedades da exibição de camada.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '54'
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

