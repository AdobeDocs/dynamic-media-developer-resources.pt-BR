---
title: Resumo do ativo
description: Resultados da pesquisa de metadados que contêm informações resumidas sobre um ativo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# [!DNL AssetSummary]{#assetsummary}

Resultados da pesquisa de metadados que contêm informações resumidas sobre um ativo.

Sintaxe

## Parâmetros {#section-ebc75cc024d94c439260d2e71873cc74}

| Nome | Tipo | Descrição |
|---|---|---|
| assetHandle | `xsd:string` | Identificador de ativo. |
| type | `xsd:string` | Tipo de ativo. A constante &quot;Tipos de ativos&quot; define os valores possíveis. Opcional. |
| name | `xsd:string` | Nome do ativo. Opcional. |
| pasta | `xsd:string` | A pasta que contém o ativo. |
| filename | `xsd:string` | Nome do arquivo do ativo. |
| criado | `xsd:dateTime` | Data de criação do ativo. |
| createUser | `xsd:string` | O usuário que criou o ativo. |
| lastModified | `xsd:dateTime` | A data em que o ativo foi atualizado pela última vez. |
| lastModifyUser | `xsd:string` | O último usuário que modificou o ativo. |
| metadataArray | `types:MetadataArray` | Uma matriz de valores de metadados associados ao ativo. |
| pontuação | `xsd:double` | Define a precisão se houver uma pesquisa de similaridade (0 = sem correspondência, 1 = correspondência exata). |
| scoreDetail | `xsd:string` | Ele contém informações detalhadas sobre áreas semelhantes como resultado de uma pesquisa de similaridade. |
