---
description: Obtém os caminhos de arquivo originais dos ativos de uma empresa.
solution: Experience Manager
title: getOriginalFilePaths
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# getOriginalFilePaths{#getoriginalfilepaths}

Obtém os caminhos de arquivo originais dos ativos de uma empresa.

Sintaxe

## Tipos de usuário autorizados {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Requer acesso de leitura ao ativo.

## Parâmetros {#section-a6b394daba6e49a8882cf3051035d9d1}

**Entrada (getOriginalFilePathsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O nome da empresa. |
| `*`assetHandleArray`*` | `types:HandleArray` | Sim | Matriz de ativos que usam o caminho de arquivo original que você deseja obter. |

**Saída (getOriginalFilePathsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`originalFileArray`*` | `types:StringArray` | Sim | A matriz de sequências de caracteres que representam os caminhos de arquivo originais. |

## Exemplos {#section-a966e783a2ba49f5b6b0f961329ab2f8}

Essa amostra de código retorna os caminhos de arquivo dos ativos especificados com identificadores de ativos exclusivos em uma matriz de manipulador de ativos.

**Solicitação**

```java
<ns1:getOriginalFilePathsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandleArray>
      <ns1:items>24265|1|17061</ns1:items>
      <ns1:items>24267|1|17063</ns1:items>
   </ns1:assetHandleArray>
</ns1:getOriginalFilePathsParam>
```

**Resposta**

```java
<getOriginalFilePathsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <originalFileArray>
      <items>MyCompany/Autumn Leaves.jpg</items>
      <items>MyCompany/Desert Landscape.jpg</items>
   </originalFileArray>
</getOriginalFilePathsReturn>
```

