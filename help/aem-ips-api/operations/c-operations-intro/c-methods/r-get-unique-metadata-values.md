---
description: Obtém valores de campo de metadados exclusivos.
solution: Experience Manager
title: getUniqueMetadataValues
feature: Dynamic Media Classic, SDK/API, Metadados
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 1%

---


# getUniqueMetadataValues{#getuniquemetadatavalues}

Obtém valores de campo de metadados exclusivos.

Sintaxe

## Tipos de usuário autorizados {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-b9d1413811c24566b6d095701f0f66db}

**Entrada (getUniqueMetadataValuesParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Manipule a empresa. |
| `*`fieldHandle`*` | `xsd:string` | Não | Lida com o campo de metadados. |

**Saída (getUniqueMetadataValuesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`values`*` | `type:StringArray` |  |  |

## Exemplos {#section-440f3bc3e5be436cb6ec26117d05f476}

Essa amostra de código usa um identificador de campo para retornar valores de metadados específicos.

**Solicitação**

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**Resposta**

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```

