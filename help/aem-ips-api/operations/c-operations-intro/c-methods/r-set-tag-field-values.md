---
description: Define os valores do dicionário de tags para um campo de tag existente.
seo-description: Define os valores do dicionário de tags para um campo de tag existente.
seo-title: setTagFieldValues
solution: Experience Manager
title: setTagFieldValues
uuid: 56666c00-3694-4a43-a0ff-97af45c8df9f
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '98'
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
