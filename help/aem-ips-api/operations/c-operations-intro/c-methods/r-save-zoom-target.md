---
description: Crie ou edite um direcionamento de zoom.
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 1%

---

# saveZoomTarget{#savezoomtarget}

Crie ou edite um direcionamento de zoom.

Sintaxe

## Tipo de usuário autorizado {#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-4a23983cae4e49a098e9bbe736933996}

**Entrada (saveZoomTargetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa com o direcionamento de zoom que você deseja salvar. |
| `*`assetHandle`*` | `xsd:string` | Sim | A alça para o destino de zoom. |
| `*`zoomTargetHandle`*` | `xsd:string` | Não | Edita ou cria um direcionamento de zoom. |
| `*`name`*` | `xsd:string` | Sim | Nome da meta de zoom. |
| `*`xPosition`*` | `xsd:int` | Sim | Localização de pixel esquerdo. |
| `*`yPosition`*` | `xsd:int` | Sim | Localização dos pixels principais. |
| `*`width`*` | `xsd:int` | Sim | Ampliação da largura de destino. |
| `*`altura`*` | `xsd:int` | Sim | Altura da meta de zoom. |
| `*`userData`*` | `xsd:string` | Sim | Para obter informações específicas do cliente. Pode conter qualquer tipo de dados. |

**Saída (saveZoomTargetReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`zoomTargetHandle`*` | `xsd:string` | Sim | Manipule o destino de zoom recém-criado. |

## Exemplos {#section-509c472c316549cdb228d7e1cfa8400a}

Essa amostra de código salva um destino de zoom. A resposta retorna a alça de destino de zoom.

**Solicitação**

```java
<saveZoomTargetParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <name>My Zoom Target</name>
   <xPosition>2</xPosition>
   <yPosition>2</yPosition>
   <width>10</width>
   <height>10</height>
   <userData>My User Data</userData>
</saveZoomTargetParam>
```

**Resposta**

```java
<saveZoomTargetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <zoomTargetHandle>34194|9|301</zoomTargetHandle>
</saveZoomTargetReturn>
```
