---
description: Caminho do arquivo de dados. Caminho relativo e nome para arquivos de dados que não sejam de imagem associados a essa imagem.
seo-description: Caminho do arquivo de dados. Caminho relativo e nome para arquivos de dados que não sejam de imagem associados a essa imagem.
seo-title: AuxPath
solution: Experience Manager
title: AuxPath
topic: Scene7 Image Serving - Image Rendering API
uuid: 95d28f8d-27ec-480a-a62a-7e5e8fbfb3fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# AuxPath{#auxpath}

Caminho do arquivo de dados. Caminho relativo e nome para arquivos de dados que não sejam de imagem associados a essa imagem.

O servidor combina esse valor com o atributo::RootPath para criar o caminho do arquivo real. Pode também ser um caminho de arquivo absoluto.

Usado para especificar um arquivo de estilo de gabinete para um material de gabinete ou um arquivo de estilo de cobertura de janela para um material de cobertura de janela. Deixe em branco para todos os outros materiais.

## Propriedades {#section-4268350054b7421da0ce0327f0731a52}

Valor da string de texto. Se especificado, deve ser um caminho de arquivo relativo ou absoluto válido. Obrigatório para materiais de armário e materiais de revestimento de janelas. Deve estar vazio para todos os outros materiais.

## Padrão {#section-287005c2d8e948fa958f69ba7b90b437}

Nenhum.

## Consulte também {#section-e1f7a61c00d04a80af28e2e67481ab92}

[atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) ,  [catálogo::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
