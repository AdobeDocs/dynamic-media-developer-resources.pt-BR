---
description: Caminho do arquivo de imagem.
solution: Experience Manager
title: Caminho
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Caminho{#path}

Caminho do arquivo de imagem.

Caminho relativo ou absoluto e nome do arquivo de imagem de origem associado a este registro de catálogo. O servidor usa as regras de resolução de caminho descritas em Gerenciamento de dados do Source para localizar o arquivo de dados.

## Propriedades {#path-properties}

String de texto. Necessário para registros de imagem, pode estar vazio para registros de modelo. Se especificado, deve ser um caminho de arquivo relativo ou absoluto do Servidor de imagens. attribute::DefaultExt será anexado se nenhum sufixo de arquivo estiver presente.

## Formatos de arquivo de imagem compatíveis {#path-supported-image-file-formats}

Consulte a descrição do utilitário Conversor de imagens (IC) para obter uma lista completa dos formatos de arquivo suportados.

Os aplicativos que exigem dados de imagem em várias resoluções diferentes têm melhor desempenho ao usar o formato de várias resoluções PTIFF (Dynamic Media pyramid TIFF). O utilitário IC é usado para criar imagens PTIFF de qualquer formato de imagem suportado.

## Padrão {#path-default}

Nenhum.

## Consulte também {#path-seealso}

[Utilitário IC](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [atributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [atributo::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
