---
description: Mensagem detalhada que responde a um dos URLs fornecidos na solicitação de invalidação CDN.
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%

---

# OperationFault{#operationfault}

Mensagem detalhada que responde a um dos URLs fornecidos na solicitação de invalidação CDN.

**Suportado desde**

4.5.0, patch 2011-02

## Parâmetros {#section-cf4b0c923cef4c14869319af73ace58b}

| ** Nome** | ** Tipo** | ** Descrição** |
|---|---|---|
| `*`código`*` | `xsd:int` | Código de erro fornecido pelo CDN |
| `*`reason`*` | `xsd:string` | Mensagem de erro fornecida pela CDN |
