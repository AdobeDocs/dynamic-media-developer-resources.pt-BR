---
description: Informações do log de trabalhos.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 0%

---

# JobLogDetail{#joblogdetail}

Informações do log de trabalhos.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| logMessage | `xsd:string` | Mensagens no log de tarefas. |
| logType | `xsd:string` | Tipo de arquivo de log da tarefa. |
| assetName | `xsd:string` | Nome do ativo no log de trabalho (opcional). |
| assetType | `xsd:string` | Escolha do tipo de ativo. |
| assetHandle | `xsd:string` | Identificador de ativo referenciado no log de trabalho. |
| auxArray | `types:JobLogDetailAuxArray` | Fornece informações adicionais detalhadas sobre o log de trabalhos além dos cinco tipos de log de trabalhos descritos acima. |
