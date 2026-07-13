---
description: Um tipo de conjunto de propriedades especifica várias configurações usadas para ajudar a gerenciar conjuntos de propriedades.
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
TQID: 'https://experienceleague.adobe.com/JOAxK9j-P0v8inQRU65C2rVCM9-OnXTXCF6wtp6eksY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 156
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
| companyHandle | `xsd:string` | Não | O identificador da empresa proprietária do tipo de conjunto de propriedades. Se `companyHandle` não for transmitido e o chamador for `IpsAdmin`, um tipo de conjunto de propriedades global será criado. |
| name | `xsd:string` | Sim | O nome do tipo de conjunto de propriedades. |
| propertyType | `xsd:string` | Sim | Escolha dos tipos de conjunto de propriedades. |
| allowMultiple | `xsd:boolean` | Sim | Determina se seu programa pode ter vários conjuntos de propriedades. |

**Saída (createPropertySetTypeReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| typeHandle | `xsd:string` | Sim | Um identificador para o tipo. |

## Exemplos {#section-13396c9639a6475190e622eae3cdb534}

Esta amostra de código cria um conjunto de propriedades com um nome e tipo especificados pela constante `PropertySet Types`. O identificador da empresa proprietária do tipo de conjunto de propriedades. Se companyHandle não for transmitido e o chamador for um IpsAdmin, um tipo de conjunto de propriedades globais será criado.

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

