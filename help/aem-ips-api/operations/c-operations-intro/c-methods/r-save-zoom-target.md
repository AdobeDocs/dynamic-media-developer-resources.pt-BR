---
description: Crie ou edite um público alvo de zoom.
seo-description: Crie ou edite um público alvo de zoom.
seo-title: saveZoomTarget
solution: Experience Manager
title: saveZoomTarget
topic: Dynamic Media Image Production System API
uuid: 197f7a2a-39ea-41cc-8e3a-76f9fe1b37d0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 1%

---


# saveZoomTarget{#savezoomtarget}

Crie ou edite um público alvo de zoom.

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
| `*`companyHandle`*` | `xsd:string` | Sim | A alça da empresa com o público alvo de zoom que você deseja salvar. |
| `*`assetHandle`*` | `xsd:string` | Sim | A alça do público alvo de zoom. |
| `*`zoomTargetHandle`*` | `xsd:string` | Não | Edita ou cria um público alvo de zoom. |
| `*`name`*` | `xsd:string` | Sim | Nome do público alvo de zoom. |
| `*`xPosition`*` | `xsd:int` | Sim | Localização do pixel esquerdo. |
| `*`yPosition`*` | `xsd:int` | Sim | Localização do pixel superior. |
| `*`width`*` | `xsd:int` | Sim | Zoom na largura do público alvo. |
| `*`altura`*` | `xsd:int` | Sim | Aumenta o zoom da altura do público alvo. |
| `*`userData`*` | `xsd:string` | Sim | Para obter informações específicas do cliente. Pode conter qualquer tipo de dados. |

**Saída (saveZoomTargetReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`zoomTargetHandle`*` | `xsd:string` | Sim | Manuseie o público alvo de zoom recém-criado. |

## Exemplos {#section-509c472c316549cdb228d7e1cfa8400a}

Essa amostra de código salva um público alvo de zoom. A resposta retorna a alça do público alvo de zoom.

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

