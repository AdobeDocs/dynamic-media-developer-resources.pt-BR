---
description: Caminho do arquivo de imagem. Caminho relativo e nome de um arquivo de imagem de textura ou decalque.
solution: Experience Manager
title: Caminho *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
TQID: 'https://experienceleague.adobe.com/ndDZ1MOPM1GHqOKFkwwMnJoZHVjaCeVVEHudb-5fPk0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 208
ht-degree: 0%

---

# Caminho *{#path}

Caminho do arquivo de imagem. Caminho relativo e nome de um arquivo de imagem de textura ou decalque.

O servidor combina esse valor com `attribute::RootPath` para criar o caminho real do arquivo de imagem. Também pode ser um caminho absoluto.

Usado para especificar o arquivo de imagem de textura para textura, gabinete e materiais de revestimento de janelas, e o arquivo de imagem RGB ou RGBA para materiais de borda de decalque e parede. Nem todos os materiais de revestimento de gabinetes e janelas exigem uma imagem de textura repetível separada.

## Propriedades {#section-8c12ea24f21d4472be677581893e6681}

String de texto. Necessário para materiais de textura e decalque, opcional para materiais de revestimento de gabinete e janela. Se especificado, deve ser um caminho de arquivo relativo ou absoluto válido. Deve estar vazio para materiais de cor sólida.

## Formatos de arquivo não suportados {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

A Renderização de imagem é compatível com os mesmos formatos de imagem de origem que o Dynamic Media Image Serving.

Os aplicativos que exigem dados de imagem em várias resoluções diferentes têm melhor desempenho ao usar o formato de várias resoluções PTIFF (Dynamic Media pyramid TIFF). O Servidor de imagens inclui o utilitário Conversor de imagens (IC), que cria imagens PTIFF de qualquer formato compatível.

Consulte a descrição do utilitário IC na documentação do Servidor de imagens para obter uma lista completa dos formatos de arquivo suportados.

## Padrão {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Nenhum.

## Consulte também {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[Utilitário IC](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [atributo::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md), [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)

