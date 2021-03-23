---
description: Remove valores de campo de tag do dicionário de um campo de tag.
seo-description: Remove valores de campo de tag do dicionário de um campo de tag.
seo-title: deleteTagFieldValues
solution: Experience Manager
title: deleteTagFieldValues
uuid: 71cdec4e-c1d6-4518-87ed-5c47a5112b15
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# deleteTagFieldValues{#deletetagfieldvalues}

Remove valores de campo de tag do dicionário de um campo de tag.

## Tipos de usuário autorizados {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-5db64a6ae238426395bc760b83587260}

**Entrada (deleteTagFieldValuesParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que contém o campo de tag. |
| `*`fieldHandle`*` | `xsd:string` | Sim | O identificador do campo de tag a ser modificado. |
| `*`valueArray`*` | `types:StringArray` | Sim | Uma matriz de valores de tag a serem excluídos do dicionário do campo. |

**Saída (deleteTagFieldValuesParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-92f9e575a6da491caa09e264b4d6ee55}

**Solicitação**

```java
deleteTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</deleteTagFieldValuesParam>
```

**Resposta**

Nenhum.
