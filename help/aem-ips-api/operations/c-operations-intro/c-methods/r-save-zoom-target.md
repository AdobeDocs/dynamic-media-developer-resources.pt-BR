---
description: Criar ou editar um destino de zoom.
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
TQID: 'https://experienceleague.adobe.com/rw-joRwkyumLI261ifPiWTeIgy4mvx-4MpgmaKcX5-E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# saveZoomTarget{#savezoomtarget}

Criar ou editar um destino de zoom.

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
| companyHandle | `xsd:string` | Sim | O identificador da empresa com o destino de zoom que você deseja salvar. |
| assetHandle | `xsd:string` | Sim | A alça para o destino de zoom. |
| zoomTargetHandle | `xsd:string` | Não | Edita ou cria um destino de zoom. |
| name | `xsd:string` | Sim | Nome do destino de zoom. |
| xPosition | `xsd:int` | Sim | Localização do pixel esquerdo. |
| yPosition | `xsd:int` | Sim | Localização do pixel superior. |
| largura | `xsd:int` | Sim | Largura de destino do zoom. |
| altura | `xsd:int` | Sim | Altura de destino do zoom. |
| userData | `xsd:string` | Sim | Para obter informações específicas do cliente. Pode conter qualquer tipo de dados. |

**Saída (saveZoomTargetReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| zoomTargetHandle | `xsd:string` | Sim | Processe o destino de zoom recém-criado. |

## Exemplos {#section-509c472c316549cdb228d7e1cfa8400a}

Esta amostra de código salva um destino de zoom. A resposta retorna o identificador do destino de zoom.

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
