---
description: Um tipo de conjunto de propriedades especifica várias configurações usadas para ajudar a gerenciar conjuntos de propriedades.
seo-description: Um tipo de conjunto de propriedades especifica várias configurações usadas para ajudar a gerenciar conjuntos de propriedades.
seo-title: createPropertySetType
solution: Experience Manager
title: createPropertySetType
topic: Dynamic Media Image Production System API
uuid: ecbaad48-d725-4f7a-a37d-5e4cde3295cb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# createPropertySetType{#createpropertysettype}

Um tipo de conjunto de propriedades especifica várias configurações usadas para ajudar a gerenciar conjuntos de propriedades.

Sintaxe

## Tipos de usuário autorizados {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-43dece72eb9f44df80f4a119dd2c008b}

**Entrada (createPropertySetTypeParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Não | O identificador da empresa proprietária do tipo de conjunto de propriedades. Se `companyHandle` não for transmitido e o chamador for `IpsAdmin`, um tipo de conjunto de propriedades global será criado. |
| `*`name`*` | `xsd:string` | Sim | O nome do tipo de conjunto de propriedades. |
| `*`propertyType`*` | `xsd:string` | Sim | Escolha dos tipos de conjunto de propriedades. |
| `*`allowMultiple`*` | `xsd:boolean` | Sim | Determina se o programa pode ter vários conjuntos de propriedades. |

**Saída (createPropertySetTypeReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Sim | Um identificador do tipo. |

## Exemplos {#section-13396c9639a6475190e622eae3cdb534}

Essa amostra de código cria um conjunto de propriedades com um nome e um tipo especificados pela constante `PropertySet Types`. O identificador da empresa proprietária do tipo de conjunto de propriedades. Se companyHandle não for transmitido e o chamador for um IpsAdmin, um tipo de conjunto de propriedades global será criado.

**Solicitação**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10803</typeHandle>
</createPropertySetTypeReturn>
```

**Resposta**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</createPropertySetTypeReturn>
```

