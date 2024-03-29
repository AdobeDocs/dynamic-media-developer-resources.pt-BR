---
description: Obtém as cadeias de caracteres de pesquisa, palavras-chave e outras informações sobre um ativo. A resposta contém informações adicionais sobre o ativo.
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---

# getSearchStrings{#getsearchstrings}

Obtém as cadeias de caracteres de pesquisa, palavras-chave e outras informações sobre um ativo. A resposta contém informações adicionais sobre o ativo.

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
| companyHandle | `xsd:string` | Sim | Processe a empresa. |
| assetHandle | `xsd:string` | Sim | Identificar o ativo. |

**Saída (getSearchStringsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| searchStringArray | `types:SearchStrings` | Sim | Uma matriz de sequências de caracteres de pesquisa de ativos. |

## Exemplos {#section-e1f73bff6e4440c489d59cb9aa5384d8}

Esta amostra de código retorna sequências de pesquisa específicas do ativo. A resposta retorna uma matriz vazia.

**Solicitação**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**Resposta**

Nenhum.
