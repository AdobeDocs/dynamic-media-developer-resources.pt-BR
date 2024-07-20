---
description: Caminho
solution: Experience Manager
title: Caminho
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f2d17309-c4d0-477f-a8d8-b40f05a1a60b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# Caminho{#path}

O servidor usa as regras de resolução de caminho descritas em [Gerenciando Dados do Source](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) para localizar o arquivo de dados.

## Propriedades {#section-72d9edc532ad43349afcb4df22e1c692}

String de texto. Necessário para registros de imagem e SVG, pode estar vazio para registros de modelo. Se especificado, deve ser um caminho de arquivo relativo ou absoluto do Servidor de imagens. attribute::DefaultExt será anexado se nenhum sufixo de arquivo estiver presente.

## Formatos de arquivo de imagem compatíveis {#section-8d6443c883aa48aaa00316fe9661aaa8}

Consulte a descrição do utilitário Conversor de imagens (IC) para obter uma lista completa dos formatos de arquivo de imagem suportados.

Os aplicativos que exigem dados de imagem em várias resoluções diferentes têm melhor desempenho ao usar o formato de multiresolução PTIFF (Dynamic Media pyramid TIFF). O utilitário IC é usado para criar imagens PTIFF de qualquer formato de imagem suportado.

## Padrão {#section-82dad83ec3f84ae8bf2f850b4139f63e}

Nenhum.

## Consulte também {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[Utilitário IC](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [atributo::RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [atributo::DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0), [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
