---
description: Propriedades do arquivo PostScript.
seo-description: Propriedades do arquivo PostScript.
seo-title: GenerationInfo
solution: Experience Manager
title: GenerationInfo
topic: Dynamic Media Image Production System API
uuid: 166637e5-b981-4f64-8d92-5fce4f1b20d2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 0%

---


# GenerationInfo{#generationinfo}

Propriedades do arquivo PostScript.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`motor`*` | `xsd:string` | Mecanismo de geração usado (consulte &quot;Informações de geração&quot; para obter os valores). |
| `*`originador`*` | `types:Asset` | Registro de ativo do ativo principal usado na geração. |
| `*`gerado`*` | `types:Asset` | Registro de ativo do ativo gerado. |
| `*`attributeArray`*` | `types:GenerationAttributeArray` | Matriz de atributos associados ao processo de geração. |

