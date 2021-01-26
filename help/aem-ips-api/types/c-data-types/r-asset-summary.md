---
description: Resultados da pesquisa de metadados que contêm informações resumidas sobre um ativo.
seo-description: Resultados da pesquisa de metadados que contêm informações resumidas sobre um ativo.
seo-title: AssetSummary
solution: Experience Manager
title: AssetSummary
topic: Dynamic Media Image Production System API
uuid: 0ac8f900-c16c-409d-b83c-3bdf0ad28fac
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 2%

---


# AssetSummary{#assetsummary}

Resultados da pesquisa de metadados que contêm informações resumidas sobre um ativo.

Sintaxe

## Parâmetros {#section-ebc75cc024d94c439260d2e71873cc74}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Identificador de ativos. |
| `*`type`*` | `xsd:string` | Tipo de ativo. A constante &quot;Tipos de ativos&quot; define os valores possíveis. Opcional. |
| `*`name`*` | `xsd:string` | Nome do ativo. Opcional. |
| `*`pasta`*` | `xsd:string` | A pasta que contém o ativo. |
| `*`nome`*` | `xsd:string` | Nome do arquivo do ativo. |
| `*`created`*` | `xsd:dateTime` | Data de criação do ativo. |
| `*`createUser`*` | `xsd:string` | O usuário que criou o ativo. |
| `*`lastModified`*` | `xsd:dateTime` | A data em que o ativo foi atualizado pela última vez. |
| `*`lastModifyUser`*` | `xsd:string` | O último usuário que modificou o ativo. |
| `*`metadataArray`*` | `types:MetadataArray` | Matriz de valores de metadados associados ao ativo. |
| `*`pontuação`*` | `xsd:double` | Define a precisão no caso de uma pesquisa de similaridade (0 = sem correspondência, 1 = correspondência exata). |
| `*`scoreDetail`*` | `xsd:string` | Retém informações detalhadas sobre áreas semelhantes como resultado de uma pesquisa de similaridade. |

