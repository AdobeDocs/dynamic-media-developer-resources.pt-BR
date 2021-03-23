---
description: Adiciona novos valores de tag ao dicionário de um campo de tag existente.
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---


# addTagFieldValues{#addtagfieldvalues}

Adiciona novos valores de tag ao dicionário de um campo de tag existente.

Sintaxe

## Tipos de usuário autorizados {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Entrada (addTagFieldValuesParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que contém o campo de tag. |
| `*`fieldHandle`*` | `xsd:string` | Sim | O identificador do campo de tag a ser modificado. |
| `*`valueArray`*` | `xsd:string` | Sim | Uma matriz de valores de tag para adicionar ao dicionário existente do campo. |

**Saída (addTagFieldValuesParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-c4049392f1c548f883b8b1f8f167bada}

**Solicitação**

```java
<addTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</addTagFieldValuesParam>
```

**Resposta**

Nenhum.
