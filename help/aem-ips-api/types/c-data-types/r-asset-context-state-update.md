---
title: AssetContextStateUpdate
description: Defina um novo conjunto de sinalizadores de estado de publicação para o contexto de publicação associado a um ativo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# [!DNL AssetContextStateUpdate]{#assetcontextstateupdate}

Defina um novo conjunto de sinalizadores de estado de publicação para o contexto de publicação associado a um ativo.

**Parâmetros**

| Nome | Tipo | Descrição |
|---|---|---|
| assetHandle | `xsd:string` | Manipule o ativo que deseja atualizar. |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | Uma matriz de estados de contato de publicação para o ativo que você deseja atualizar. |
