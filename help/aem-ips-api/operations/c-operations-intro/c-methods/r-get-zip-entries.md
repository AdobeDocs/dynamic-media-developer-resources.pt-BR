---
description: Retorna os dados do arquivo Zip.
solution: Experience Manager
title: getZipEntries
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: eb052685-b750-4a12-b00e-28e676340e98
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# getZipEntries{#getzipentries}

Retorna os dados do arquivo Zip.

Sintaxe

## Tipos de usuário autorizados {#section-33a3f03ba8a14086922397619ce12ab8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-aa3f498fe76d4a5f99c42d64520fadce}

**Entrada (getZipEntriesParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa que contém o arquivo Zip. |
| assetHandle | `xsd:string` | Sim | Processe o arquivo Zip. |

**Saída (getZipEntriesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| zipArray | `types:ZipEntryArray` | Sim | Matriz de entradas em um arquivo Zip. |

## Exemplos {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

Esta amostra de código retorna informações do arquivo Zip, incluindo tamanho compactado e descompactado.

**Solicitação**

```java
<getZipEntriesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|94223|27|30602</assetHandle>
</getZipEntriesParam>
```

**Resposta**

```java
<getZipEntriesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zipArray
      <items>
         <name>Checklist_Images/.DS_Store</name>
         <isDirectory>false</isDirectory>
         <lastModified>2007-05-09T15:41:52.000-07:00</lastModified>
         <compressedSize>503</compressedSize>
         <uncompressedSize>6148</uncompressedSize>
      </items>
   ...
   </zipArray>
</getZipEntriesReturn>
```
