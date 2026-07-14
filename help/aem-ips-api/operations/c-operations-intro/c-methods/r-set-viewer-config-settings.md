---
description: Anexa as configurações do visualizador a um ativo. Eles podem ser uma predefinição do visualizador ou o ativo de origem do visualizador.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
TQID: 'https://experienceleague.adobe.com/MX6dj-7j6HfNSISaWFheorOZYVnszSY24OuuUGdKvPA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 0%

---

# setViewerConfigSettings{#setviewerconfigsettings}

Anexa as configurações do visualizador a um ativo. Eles podem ser uma predefinição do visualizador ou o ativo de origem do visualizador.

Sintaxe

## Tipos de usuário autorizados {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-bcc8c83cc84141e8b1341be9133e8511}

**Entrada (setViewerConfigSettingsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | Processe a empresa. |
| assetHandle | `xsd:string` | Sim | Identificador de ativo. |
| name | `xsd:string` | Sim | Nome do ativo. |
| type | `xsd:string` | Sim | O tipo de ativo ao qual você deseja aplicar a configuração do visualizador. |
| configSettingArray | `types:ConfigSettingArray` | Sim | A matriz de `ConfigSettings` aplicada ao ativo. |

**Saída (setViewerConfigSettingsParam)**

A API do IPS não retorna uma resposta para esta operação.

