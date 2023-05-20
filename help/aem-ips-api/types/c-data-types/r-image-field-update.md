---
description: Atualiza o campo de imagem associado a um ativo de imagem.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 0%

---

# [!DNL ImageFieldUpdate]{#imagefieldupdate}

Atualiza o campo de imagem associado a um ativo de imagem.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| assetHandle | `xsd:string` | Identificador de ativo. |
| [!DNL resolution] | `xsd:double` | Resolução da imagem em pixels por polegada. |
| [!DNL anchorX] | `xsd:int` | Âncora de imagem do eixo X. |
| [!DNL anchorY] | `xsd:int` | Âncora de imagem do eixo Y. |
| [!DNL userData] | `xsd:string` | Valor de `userData` campo de metadados, que é publicado no campo de catálogo de dados do usuário do servidor de imagens. |
