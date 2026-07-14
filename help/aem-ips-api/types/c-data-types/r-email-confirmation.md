---
description: Envia um email para um recipient designado em resposta a uma operação cdnCacheInvalidation.
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
TQID: 'https://experienceleague.adobe.com/h9ZZRR0zR347mzSifomCmtNW5GorTC6fgGjeSRf52KU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 0%

---

# [!DNL EmailConfirmation]{#emailconfirmation}

Envia um email para um recipient designado em resposta a uma operação cdnCacheInvalidation.

Sintaxe

## Parâmetros {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nome | Tipo | Descrição |
|---|---|---|
| ccOriginator | `xsd:boolean` | Se verdadeiro, inclui a conta de usuário do serviço Web do usuário, que é uma lista de emails designados para receber uma confirmação por email do CDN do Dynamic Media. |
| ccOthersArray | `types:EmailArray` | Uma matriz de endereços de email (máximo de 5) designada para receber a notificação de confirmação do CDN do Dynamic Media. |

