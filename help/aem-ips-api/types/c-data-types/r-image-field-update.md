---
description: Atualiza o campo de imagem associado a um ativo de imagem.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 0%

---

# ImageFieldUpdate{#imagefieldupdate}

Atualiza o campo de imagem associado a um ativo de imagem.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| assetHandle | `xsd:string` | Identificador de ativo. |
| resolution | `xsd:double` | Resolução da imagem em pixels por polegada. |
| anchorX | `xsd:int` | Âncora de imagem do eixo X. |
| âncoraY | `xsd:int` | Âncora de imagem do eixo Y. |
| userData | `xsd:string` | Valor de `userData` campo de metadados, que é publicado no campo de catálogo de dados do usuário que serve a imagem. |
