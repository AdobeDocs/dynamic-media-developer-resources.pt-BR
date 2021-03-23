---
description: Caminho do arquivo de imagem. Caminho relativo e nome de um arquivo de imagem de textura ou decalque.
seo-description: Caminho do arquivo de imagem. Caminho relativo e nome de um arquivo de imagem de textura ou decalque.
seo-title: Caminho *
solution: Experience Manager
title: Caminho *
uuid: 9e85a358-3f2f-4b8b-a98f-03de2a1a8a4c
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# Caminho *{#path}

Caminho do arquivo de imagem. Caminho relativo e nome de um arquivo de imagem de textura ou decalque.

O servidor combina esse valor com `attribute::RootPath` para criar o caminho do arquivo de imagem real. Pode também ser um caminho absoluto.

Usado para especificar o arquivo de imagem de textura para materiais de cobertura de textura, gabinete e janela, e o arquivo de imagem RGB ou RGBA para materiais de borda de decalque e parede. Nem todos os materiais de revestimento de armário e janela exigem uma imagem de textura repetível separada.

## Propriedades {#section-8c12ea24f21d4472be677581893e6681}

Sequência de texto. Obrigatório para materiais de textura e decalque, facultativo para materiais de revestimento de armário e de janela. Se especificado, deve ser um caminho de arquivo relativo ou absoluto válido. Deve estar vazio para materiais de cor sólida.

## Formatos de arquivo compatíveis {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

A Renderização de imagem é compatível com os mesmos formatos de imagem de origem que o Dynamic Media Image Serving.

Os aplicativos que exigem dados de imagem em várias resoluções diferentes terão o melhor desempenho ao usar o formato de multiresolução TIFF (PTIFF) da pirâmide Dynamic Media. A Exibição de imagens inclui o utilitário Conversor de imagens (IC) que cria imagens PTIFF de qualquer formato compatível.

Consulte a descrição do utilitário IC na documentação do Image Serving para obter uma lista completa dos formatos de arquivo compatíveis.

## Padrão {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Nenhum.

## Consulte também {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[Utilitário](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md)  IC,  [atributo::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md),  [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
