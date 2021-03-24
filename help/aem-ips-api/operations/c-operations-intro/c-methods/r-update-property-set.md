---
description: Usa uma matriz de propriedades para atualizar um conjunto de propriedades.
solution: Experience Manager
title: updatePropertySet
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# updatePropertySet{#updatepropertyset}

Usa uma matriz de propriedades para atualizar um conjunto de propriedades.

Sintaxe

## Tipos de usuário autorizados {#section-116693bbfb5d44219e62bbb1ba19de96}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-98361b063e9c41e8b2f744fabc0e13ed}

**Entrada (updatePropertySetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Sim | Manipule para o conjunto de propriedades. |
| `*`replaceProperties`*` | `xsd:string` | Não | Defina como `true` para substituir propriedades. |
| `*`propertyArray`*` | `types:PropertyArray` | Sim | Matriz de propriedades atualizadas para o conjunto de propriedades. |

**Saída (updatePropertySetReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

Este exemplo de código atualiza um conjunto de propriedades com propriedades na matriz de propriedades.

**Solicitação**

```java
<updatePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
   <replaceProperties>true</replaceProperties>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>false</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7teton.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7teton:8080/is/image/</value>
      </items>
   </propertyArray>
</updatePropertySetParam>
```

**Resposta**

Nenhum.
