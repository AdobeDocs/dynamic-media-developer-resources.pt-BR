---
description: Informações de log do trabalho.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '60'
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
