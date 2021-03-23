---
description: Resultados da pesquisa de metadados que contêm informações resumidas sobre um ativo.
seo-description: Resultados da pesquisa de metadados que contêm informações resumidas sobre um ativo.
seo-title: AssetSummary
solution: Experience Manager
title: AssetSummary
uuid: 0ac8f900-c16c-409d-b83c-3bdf0ad28fac
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# AssetSummary{#assetsummary}

Resultados da pesquisa de metadados que contêm informações resumidas sobre um ativo.

Sintaxe

## Parâmetros {#section-ebc75cc024d94c439260d2e71873cc74}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Identificador de ativo. |
| `*`type`*` | `xsd:string` | Tipo de ativo. A constante &quot;Tipos de ativo&quot; define os valores possíveis. Opcional. |
| `*`name`*` | `xsd:string` | Nome do ativo. Opcional. |
| `*`pasta`*` | `xsd:string` | A pasta que contém o ativo. |
| `*`filename`*` | `xsd:string` | Nome do arquivo do ativo. |
| `*`criado`*` | `xsd:dateTime` | Data de criação do ativo. |
| `*`createUser`*` | `xsd:string` | O usuário que criou o ativo. |
| `*`lastModified`*` | `xsd:dateTime` | A data em que o ativo foi atualizado pela última vez. |
| `*`lastModifyUser`*` | `xsd:string` | O último usuário que modificou o ativo. |
| `*`metadataArray`*` | `types:MetadataArray` | Matriz de valores de metadados associados ao ativo. |
| `*`pontuação`*` | `xsd:double` | Define a precisão no caso de uma pesquisa de semelhança (0 = sem correspondência, 1 = correspondência exata). |
| `*`scoreDetail`*` | `xsd:string` | Contém informações detalhadas sobre áreas semelhantes como resultado de uma pesquisa de semelhança. |

