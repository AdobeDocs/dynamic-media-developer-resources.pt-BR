---
description: Caminho do arquivo de imagem.
solution: Experience Manager
title: Caminho
topic: Scene7 Image Serving - Image Rendering API
uuid: 0fca88bb-de00-4eff-83ad-c0f5e3b8ece0
translation-type: tm+mt
source-git-commit: 7b837020deef888a038a074d0aa826d43e60aeb6
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Caminho{#path}

Caminho do arquivo de imagem.

Caminho relativo ou absoluto e nome do arquivo de imagem de origem associado a este registro de catálogo. O servidor usa as regras de resolução de caminho descritas em Gerenciamento de dados de origem para localizar o arquivo de dados.

## Propriedades {#path-properties}

Sequência de caracteres de texto. Obrigatório para registros de imagem, pode estar vazio para registros de modelo. Se especificado, deve ser um caminho de arquivo válido relativo ou absoluto do Servidor de imagens. atributo::DefaultExt será anexado se nenhum sufixo de arquivo estiver presente.

## Formatos de arquivo de imagem suportados {#path-supported-image-file-formats}

Consulte a descrição do utilitário Conversor de imagens (IC) para obter uma lista completa dos formatos de arquivo suportados.

Os aplicativos que exigem dados de imagem em várias resoluções diferentes terão melhor desempenho ao usar o formato de multiresolução TIFF (PTIFF) da pirâmide Dynamic Media. O utilitário IC é usado para criar imagens PTIFF a partir de qualquer formato de imagem compatível.

## Padrão {#path-default}

Nenhum.

## Consulte também {#path-seealso}

[Utilitário](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md)  IC,  [atributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [atributo::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) ,  [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->