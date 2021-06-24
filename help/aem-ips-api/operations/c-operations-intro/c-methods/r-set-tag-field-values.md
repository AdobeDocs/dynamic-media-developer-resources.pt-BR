---
description: Define os valores do dicionário de tags para um campo de tag existente.
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# setTagFieldValues{#settagfieldvalues}

Define os valores do dicionário de tags para um campo de tag existente.

Sintaxe

## Tipos de usuário autorizados {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-a05cbee4cb4f44198c414a6b14e69156}

**Entrada**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Manuseio da empresa. |
| `*`fieldHandle`*` | `xsd:string` | Sim | Identificador de campo de tag. |
| `*`valueArray`*` | `types:StringArray` | Sim | Uma matriz de valores de tag que substitui o dicionário existente do campo. As associações de ativos são mantidas quando um novo valor corresponde a um valor existente. |

**Saída (setTagFieldValuesReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-b11cafd9bed54ab5836c737cc075c918}

**Solicitação**

```java
<setTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Nurth</items>
      <items>Suth</items>
      <items>East</items>
      <items>West</items>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</setTagFieldValuesParam>
```

**Resposta**

Nenhum.
