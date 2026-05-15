---
description: Somente para uso interno. Os usuários devem consultar a seção Referência do catálogo de imagens do servidor de imagens - Referência do atributo.
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
TQID: 'https://experienceleague.adobe.com/-VBxIs4EWFDesksSnU-DpN2pg-LJUN60OPhqjQVqAr8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 0%

---

# getImageServingPublishSettings{#getimageservingpublishsettings}

Somente para uso interno. Os usuários devem consultar a seção Referência do catálogo de imagens do servidor de imagens - Referência do atributo.

Sintaxe

## Tipos de usuário autorizados {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-79f0d54acd604ad2a5c96679334f2424}

**Entrada (getImageServingPublishSettingsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa com as configurações de publicação do servidor de imagens. |
| contextHandle | `xsd:string` | Sim | Processe o contexto de publicação. |

**Saída**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| publishSettingArray | `xsd:string` | Sim | Matriz de configurações de publicação do servidor de imagens. |
