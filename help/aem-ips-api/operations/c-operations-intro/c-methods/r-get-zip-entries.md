---
description: Retorna os dados do arquivo Zip.
seo-description: Retorna os dados do arquivo Zip.
seo-title: getZipEntries
solution: Experience Manager
title: getZipEntries
uuid: cfc45f83-1cf9-4c50-9aac-5a731e62a839
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
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
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador para a empresa que contém o arquivo Zip. |
| `*`assetHandle`*` | `xsd:string` | Sim | Manipule o arquivo Zip. |

**Saída (getZipEntriesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`zipArray`*` | `types:ZipEntryArray` | Sim | Matriz de entradas em um arquivo Zip. |

## Exemplos {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

Essa amostra de código retorna informações do arquivo Zip, incluindo o tamanho compactado e descompactado.

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

