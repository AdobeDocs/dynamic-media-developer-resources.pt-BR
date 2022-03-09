---
description: Propriedades do arquivo PostScript.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 0%

---

# GenerationInfo{#generationinfo}

Propriedades do arquivo PostScript.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| motor | `xsd:string` | Mecanismo de geração usado (consulte &quot;Informações de geração&quot; para valores). |
| originador | `types:Asset` | Registro de ativo do ativo principal usado na geração. |
| gerado | `types:Asset` | Registro de ativo do ativo gerado. |
| attributeArray | `types:GenerationAttributeArray` | Matriz de atributos associados ao processo de geração. |
