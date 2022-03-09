---
title: AssetContextStateUpdate
description: Defina um novo conjunto de sinalizadores de estado de publicação para o contexto de publicação associado a um ativo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---

# AssetContextStateUpdate{#assetcontextstateupdate}

Defina um novo conjunto de sinalizadores de estado de publicação para o contexto de publicação associado a um ativo.

**Parâmetros**

| Nome | Tipo | Descrição |
|---|---|---|
| assetHandle | `xsd:string` | Manipule o ativo que deseja atualizar. |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | Uma matriz de estados de contato de publicação para o ativo que você deseja atualizar. |
