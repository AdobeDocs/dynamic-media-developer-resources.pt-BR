---
description: Caminho
solution: Experience Manager
title: Caminho
uuid: d1ed8a98-60eb-4bdb-884e-ea08c018d834
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Caminho{#path}

O servidor usa as regras de resolução de caminho descritas em [Gerenciando Dados de Origem](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) para localizar o arquivo de dados.

## Propriedades {#section-72d9edc532ad43349afcb4df22e1c692}

Sequência de texto. Necessário para registros de imagem e SVG, pode estar vazio para registros de modelo. Se especificado, deve ser um caminho de arquivo válido relativo ou absoluto do Servidor de Imagens. attribute::DefaultExt será anexado se nenhum sufixo de arquivo estiver presente.

## Formatos de arquivo de imagem compatíveis {#section-8d6443c883aa48aaa00316fe9661aaa8}

Consulte a descrição do utilitário Conversor de imagem (IC) para obter uma lista completa dos formatos de arquivo de imagem suportados.

Os aplicativos que exigem dados de imagem em várias resoluções diferentes terão o melhor desempenho ao usar o formato de multiresolução TIFF (PTIFF) da pirâmide Dynamic Media. O utilitário IC é usado para criar imagens PTIFF de qualquer formato de imagem compatível.

## Padrão {#section-82dad83ec3f84ae8bf2f850b4139f63e}

Nenhum.

## Consulte também {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[Utilitário](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b) IC,  [atributo::RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [atributo::DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0),  [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
