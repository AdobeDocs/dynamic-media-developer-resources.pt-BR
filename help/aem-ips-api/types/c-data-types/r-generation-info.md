---
description: Propriedades do arquivo PostScript.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 0%

---

# [!DNL GenerationInfo]{#generationinfo}

Propriedades do arquivo PostScript.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| [!DNL engine] | `xsd:string` | Mecanismo de geração usado (consulte &quot;Informações de geração&quot; para valores). |
| [!DNL originator] | `types:Asset` | Registro de ativo do ativo principal usado na geração. |
| [!DNL generated] | `types:Asset` | Registro de ativo do ativo gerado. |
| attributeArray | `types:GenerationAttributeArray` | Matriz de atributos associados ao processo de geração. |
