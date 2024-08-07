---
description: Caminho do arquivo de imagem. Caminho relativo e nome de um arquivo de imagem de textura ou decalque.
solution: Experience Manager
title: Caminho *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Caminho *{#path}

Caminho do arquivo de imagem. Caminho relativo e nome de um arquivo de imagem de textura ou decalque.

O servidor combina esse valor com `attribute::RootPath` para criar o caminho real do arquivo de imagem. Também pode ser um caminho absoluto.

Usado para especificar o arquivo de imagem de textura para materiais de textura, gabinete e revestimento de janelas, e o arquivo de imagem RGB ou RGBA para materiais de borda de decalque e parede. Nem todos os materiais de revestimento de gabinetes e janelas exigem uma imagem de textura repetível separada.

## Propriedades {#section-8c12ea24f21d4472be677581893e6681}

String de texto. Necessário para materiais de textura e decalque, opcional para materiais de revestimento de gabinete e janela. Se especificado, deve ser um caminho de arquivo relativo ou absoluto válido. Deve estar vazio para materiais de cor sólida.

## Formatos de arquivo não suportados {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

A Renderização de imagem é compatível com os mesmos formatos de imagem de origem que o Dynamic Media Image Serving.

Os aplicativos que exigem dados de imagem em várias resoluções diferentes têm melhor desempenho ao usar o formato de multiresolução PTIFF (Dynamic Media pyramid TIFF). O Servidor de imagens inclui o utilitário Conversor de imagens (IC), que cria imagens PTIFF de qualquer formato compatível.

Consulte a descrição do utilitário IC na documentação do Servidor de imagens para obter uma lista completa dos formatos de arquivo suportados.

## Padrão {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Nenhum.

## Consulte também {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[Utilitário IC](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [atributo::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md), [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
