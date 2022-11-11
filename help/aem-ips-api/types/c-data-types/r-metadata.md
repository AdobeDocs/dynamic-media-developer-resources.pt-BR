---
description: Um campo de metadados retornado pelo searchAssets.
solution: Experience Manager
title: Metadados
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 62e3e215-31ea-49fd-937e-d136fdf84aff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---

# [!DNL Metadata]{#metadata}

Um campo de metadados retornado pelo searchAssets.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| name | `xsd:string` | Nome dos metadados. |
| value | `xsd:string` | Valor dos metadados. |
| boolVal | `xsd:boolean` | Valor de metadados booleanos (somente para campos do tipo Booliano). |
| longVal | `xsd:long` | Valor de metadados longo (somente para campos sem tipo). |
| doubleVal | `xsd:double` | Valor de metadados duplos (somente para campos de tipo flutuante). |
| dateVal | `xsd:dateTime` | Valor dos metadados de data (somente para campos do tipo data). |
