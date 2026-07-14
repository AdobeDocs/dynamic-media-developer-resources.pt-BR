---
description: Os conjuntos de propriedades são conjuntos específicos de pares de nome-valor do aplicativo que podem ser anexados a vários objetos IPS, dependendo do tipo de conjunto de propriedades. Se o tipo de conjunto de propriedades não permitir que vários conjuntos sejam anexados a um objeto (PropertySetType/allowMultipleisfalse) e o objeto já tiver um conjunto associado do mesmo tipo, o novo conjunto substituirá o existente.
solution: Experience Manager
title: createPropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e9f85e65-4a2f-4b82-b7b8-d0d60b8345cd
TQID: 'https://experienceleague.adobe.com/kMRKY0OQPDLsPpPDtTQpxwTBiBu3dco37mSxR7khfgg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 217
ht-degree: 0%

---

# createPropertySet{#createpropertyset}

Os conjuntos de propriedades são conjuntos específicos de pares de nome-valor do aplicativo que podem ser anexados a vários objetos IPS, dependendo do tipo de conjunto de propriedades. Se o tipo de conjunto de propriedades não permitir que vários conjuntos sejam anexados a um objeto (PropertySetType/allowMultipleisfalse) e o objeto já tiver um conjunto associado do mesmo tipo, o novo conjunto substituirá o existente.

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
| typeHandle | `xsd:string` | Sim | O identificador para o tipo de conjunto de propriedades. |
| primaryOwnerHandle | `xsd:string` | Sim | O identificador para o proprietário principal do conjunto de propriedades. |
| secondaryOwnerHandle | `xsd:string` | Não | O identificador para o proprietário secundário do conjunto de propriedades. |
| propertyArray | `types:PropertyArray` | Sim | A matriz de propriedades. |
| permissionArray | `types:PermissionUpdateArray` |  |  |

**Saída (createPropertySetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| setHandle | `xsd:string` | Sim | O identificador para o novo conjunto de propriedades. |

## Exemplos {#section-4e1f5b2883664bc88f590fcd253df22b}

Esta amostra de código cria um conjunto de propriedades que contém nomes e valores de propriedades. A resposta retorna um identificador para o novo conjunto de propriedades.

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

