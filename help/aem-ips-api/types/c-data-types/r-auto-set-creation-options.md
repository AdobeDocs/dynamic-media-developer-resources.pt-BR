---
description: Lista automática de scripts de geração de conjunto para trabalhos de upload. O teste z assume que cada script especificado para o upload é aplicado a todos os ativos carregados.
solution: Experience Manager
title: AutoDefinirOpçõesDeCriação
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e6e969be-0410-4be7-88d6-491d715fd137
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---

# [!DNL AutoSetCreationOptions]{#autosetcreationoptions}

Lista automática de scripts de geração de conjunto para trabalhos de upload. O teste z assume que cada script especificado para o upload é aplicado a todos os ativos carregados.

Sintaxe

## Parâmetros {#section-0302e9238dbc4704914e938f42c881e6}

| Nome | Tipo | Descrição |
|---|---|---|
| autoSetsArray | `types:HandleArray` | Matriz de [!DNL PropertySet] identificadores definindo os scripts de geração de conjunto automático aplicados durante o carregamento. |
