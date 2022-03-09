---
description: Mensagem detalhada que responde a um dos URLs fornecidos na solicitação de invalidação CDN.
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 0%

---

# OperationFault{#operationfault}

Mensagem detalhada que responde a um dos URLs fornecidos na solicitação de invalidação CDN.

**Suportado desde**

4.5.0, patch 2011-02

## Parâmetros {#section-cf4b0c923cef4c14869319af73ace58b}

| ** Nome** | ** Tipo** | ** Descrição** |
|---|---|---|
| código | `xsd:int` | Código de erro fornecido pelo CDN |
| reason | `xsd:string` | Mensagem de erro fornecida pela CDN |
