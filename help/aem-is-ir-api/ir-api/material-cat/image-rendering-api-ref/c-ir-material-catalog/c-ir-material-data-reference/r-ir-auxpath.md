---
description: Caminho do arquivo de dados. Caminho relativo e nome para arquivos de dados que não são de imagem associados a esta imagem.
solution: Experience Manager
title: AuxPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55f82596-72f0-48c4-9b3a-f10ea5f610f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# AuxPath{#auxpath}

Caminho do arquivo de dados. Caminho relativo e nome para arquivos de dados que não são de imagem associados a esta imagem.

O servidor combina esse valor com attribute::RootPath para criar o caminho de arquivo real. Também pode ser um caminho de arquivo absoluto.

Usado para especificar um arquivo de estilo de gabinete para um material de gabinete ou um arquivo de estilo de cobertura de janela para um material de cobertura de janela. Deixe em branco para todos os outros materiais.

## Propriedades {#section-4268350054b7421da0ce0327f0731a52}

Valor da string de texto. Se especificado, deve ser um caminho de arquivo relativo ou absoluto válido. Necessário para materiais de gabinete e materiais de revestimento de janela. Deve estar vazio para todos os outros materiais.

## Padrão {#section-287005c2d8e948fa958f69ba7b90b437}

Nenhum.

## Consulte também {#section-e1f7a61c00d04a80af28e2e67481ab92}

[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) , [catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
