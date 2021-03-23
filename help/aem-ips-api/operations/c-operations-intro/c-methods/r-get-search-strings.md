---
description: Obtém as sequências de pesquisa, palavras-chave e outras informações sobre um ativo. A resposta contém informações adicionais sobre o ativo.
seo-description: Obtém as sequências de pesquisa, palavras-chave e outras informações sobre um ativo. A resposta contém informações adicionais sobre o ativo.
seo-title: getSearchStrings
solution: Experience Manager
title: getSearchStrings
uuid: 9d588d6b-c79c-4531-a2e8-8467254a7985
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# getSearchStrings{#getsearchstrings}

Obtém as sequências de pesquisa, palavras-chave e outras informações sobre um ativo. A resposta contém informações adicionais sobre o ativo.

Sintaxe

## Tipos de usuário autorizados {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-c1efda4bb15349a68b276bafee8c18fd}

**Entrada (getSearchStringsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Manipule a empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | Lidar com o ativo. |

**Saída (getSearchStringsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`searchStringArray`*` | `types:SearchStrings` | Sim | Uma matriz de cadeias de caracteres de pesquisa de ativos. |

## Exemplos {#section-e1f73bff6e4440c489d59cb9aa5384d8}

Essa amostra de código retorna cadeias de pesquisa específicas do ativo. A resposta retorna uma matriz vazia.

**Solicitação**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**Resposta**

Nenhum.
