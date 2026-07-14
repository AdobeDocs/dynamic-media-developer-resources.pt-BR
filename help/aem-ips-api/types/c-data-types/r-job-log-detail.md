---
description: Informações de log do trabalho.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
TQID: 'https://experienceleague.adobe.com/wH0F5TxaTHxn-vP7PTri94WxEa5Bs9Q2-CRnuHdVb3I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 0%

---

# [!DNL JobLogDetail]{#joblogdetail}

Informações de log do trabalho.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| logMessage | `xsd:string` | Mensagens no registro de tarefas. |
| logType | `xsd:string` | Tipo de arquivo de log do trabalho. |
| assetName | `xsd:string` | Nome do ativo no log de trabalho (opcional). |
| assetType | `xsd:string` | Escolha do tipo de ativo. |
| assetHandle | `xsd:string` | Identificador de ativo referenciado no log de trabalho. |
| auxArray | `types:JobLogDetailAuxArray` | Fornece informações adicionais detalhadas sobre o registro do trabalho além dos cinco tipos de registro do trabalho descritos acima. |

