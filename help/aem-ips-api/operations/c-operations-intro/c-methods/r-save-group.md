---
description: Crie ou edite um grupo.
seo-description: Crie ou edite um grupo.
seo-title: saveGroup
solution: Experience Manager
title: saveGroup
uuid: d1631a55-7f1d-48b4-8b35-fd5a05277219
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# saveGroup{#savegroup}

Crie ou edite um grupo.

Sintaxe

## Tipos de usuário autorizados {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-743610e98dd5494baffcbad6401038eb}

**Entrada (saveGroupParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa com o grupo que você deseja salvar. |
| `*`groupHandle`*` | `xsd:string` | Não | O identificador do grupo. |
| `*`name`*` | `xsd:string` | Sim | Nome do grupo. |
| `*`isSystemDefined`*` | `xsd:boolean` | Sim | `false` é padrão. |

**Saída (saveGroupReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`groupHandle`*` | `xsd:string` | Sim | Identificador de grupo. |

## Exemplos {#section-26eee227ff1f4edabb7fa1240b4d9999}

Essa amostra de código cria um grupo que pertence a uma empresa específica. Se o grupo já existir, ele será salvo com os valores de parâmetro especificados.

**Solicitação**

```java
<ns1:saveGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:name>My Other Group</ns1:name>
   <ns1:isSystemDefined>false</ns1:isSystemDefined>
</ns1:saveGroupParam>
```

**Resposta**

```java
<saveGroupReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupHandle>281</groupHandle>
</saveGroupReturn>
```

