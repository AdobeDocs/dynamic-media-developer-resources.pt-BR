---
description: Identificador do registro do catálogo
solution: Experience Manager
title: Id
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9803d754-1f94-4e5d-9a40-3936676c0035
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---


# Id {#id}

Valor da chave de índice pelo qual os registros no arquivo de dados da imagem são pesquisados pelo Servidor de plataforma.

Normalmente, um identificador de imagem curto e exclusivo, como um número SKU, possivelmente com algum tipo de sufixo de imagem, se um SKU tiver várias imagens. Pode também ser uma sequência de caracteres mais complexa que se pareça mais com um caminho de arquivo, para suportar a fácil adaptação de sites com o Serviço de imagem.

## Propriedades {#id-properties}

Sequência de caracteres de texto. Obrigatório. Chave de índice primária para a tabela de dados da imagem. Cada valor de catálogo::Id deve ser exclusivo na tabela.

## Padrão {#id-default}

Nenhum.

## Consulte também {#id-seealso}

[atributo::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)