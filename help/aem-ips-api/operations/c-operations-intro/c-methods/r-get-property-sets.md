---
description: Obtém conjuntos de propriedades associados a um identificador de tipo.
solution: Experience Manager
title: getPropertySets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da6923c3-9b86-4595-8205-645fb10e03b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# getPropertySets{#getpropertysets}

Obtém conjuntos de propriedades associados a um identificador de tipo.

Sintaxe

## Tipos de usuário autorizados {#section-da858360b72941bfa8d9558b4da7d4da}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-d8da2847e77e4a95a4441d9848cac775}

**Entrada (getPropertySetsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| typeHandle | `xsd:string` | Sim | O identificador para o tipo de conjunto de propriedades. |
| primaryOwnerHandle | `xsd:string` | Sim | O proprietário principal dos dados associados ao objeto de banco de dados. |
| secondaryOwnerHandle | `xsd:string` | Não | Um proprietário secundário opcional dos dados. |

**Saída (getPropertySetsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| setArray | `types:PropertySetArray` | Sim | Matriz de conjuntos de propriedades. |

## Exemplos {#section-1358af974eab4259864910337a6f0bd2}

Essa amostra de código retorna conjuntos de propriedades do proprietário principal, especificados por um identificador de tipo.

**Solicitação**

```java
<getPropertySetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
</getPropertySetsParam>
```

**Resposta**

```java
<getPropertySetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setArray>
      <items>
         <setHandle>ps|941</setHandle>
         <typeHandle>pt|10801</typeHandle>
         <propertyArray>
            <items>
               <name>application_server_prefix_published_test</name>
               <value>http://s7teton.macromedia.com:8080/is/image/</value>
            </items>
            <items>
               <name>application_project_whatever</name>
               <value>false</value>
            </items>
            <items>
               <name>application_server_prefix_origin_test</name>
               <value>http://s7teton:8080/is/image</value>
            </items>
         </propertyArray>
      </items>
   </setArray>
</getPropertySetsReturn>
```
