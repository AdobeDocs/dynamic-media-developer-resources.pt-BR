---
description: Os conjuntos de propriedades são conjuntos específicos do aplicativo de pares de nome-valor que podem ser anexados a vários objetos IPS, dependendo do tipo de conjunto de propriedades. Se o tipo de conjunto de propriedades não permitir que vários conjuntos sejam anexados a um objeto (PropertySetType/allowMultipleisfalse) e o objeto já tiver um conjunto associado do mesmo tipo, o novo conjunto substituirá o existente.
seo-description: Os conjuntos de propriedades são conjuntos específicos do aplicativo de pares de nome-valor que podem ser anexados a vários objetos IPS, dependendo do tipo de conjunto de propriedades. Se o tipo de conjunto de propriedades não permitir que vários conjuntos sejam anexados a um objeto (PropertySetType/allowMultipleisfalse) e o objeto já tiver um conjunto associado do mesmo tipo, o novo conjunto substituirá o existente.
seo-title: createPropertySet
solution: Experience Manager
title: createPropertySet
uuid: f0b5b951-143f-4a31-bb6b-cdeabdebbcbb
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---


# createPropertySet{#createpropertyset}

Os conjuntos de propriedades são conjuntos específicos do aplicativo de pares de nome-valor que podem ser anexados a vários objetos IPS, dependendo do tipo de conjunto de propriedades. Se o tipo de conjunto de propriedades não permitir que vários conjuntos sejam anexados a um objeto (PropertySetType/allowMultipleisfalse) e o objeto já tiver um conjunto associado do mesmo tipo, o novo conjunto substituirá o existente.

Sintaxe

## Tipos de usuário autorizados {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-25258e75f5f3419bad165c797eb6cd8e}

**Entrada (createPropertySetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Sim | O identificador do tipo de conjunto de propriedades. |
| `*`primaryOwnerHandle`*` | `xsd:string` | Sim | O identificador do proprietário principal do conjunto de propriedades. |
| `*`secondaryOwnerHandle`*` | `xsd:string` | Não | O identificador para o proprietário secundário do conjunto de propriedades. |
| `*`propertyArray`*` | `types:PropertyArray` | Sim | A matriz de propriedades. |
| `*`permissionArray`*` | `types:PermissionUpdateArray` |  |  |

**Saída (createPropertySetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Sim | O identificador do novo conjunto de propriedades. |

## Exemplos {#section-4e1f5b2883664bc88f590fcd253df22b}

Essa amostra de código cria um conjunto de propriedades que contém nomes e valores de propriedades. A resposta retorna um identificador para o novo conjunto de propriedades.

**Solicitação**

```java
<createPropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>true</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7everest.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7everest:8080/is/image/</value>
      </items>
   </propertyArray>
</createPropertySetParam>
```

**Resposta**

```java
<createPropertySetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</createPropertySetReturn>
```

