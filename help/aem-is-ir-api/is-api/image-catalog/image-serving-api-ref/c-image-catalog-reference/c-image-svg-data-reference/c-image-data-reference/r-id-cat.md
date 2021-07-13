---
description: Identificador do registro de catálogo
solution: Experience Manager
title: Id
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# Id {#id}

Valor da chave de índice pelo qual os registros no arquivo de dados de imagem são pesquisados pelo Servidor de plataforma.

Normalmente, um identificador de imagem curto e exclusivo, como um número SKU, possivelmente com algum tipo de sufixo de imagem, se um SKU tiver várias imagens. Pode também ser uma sequência de caracteres mais complexa, mais parecida com um caminho de arquivo, para oferecer suporte à fácil remontagem de sites com o Serviço de imagem.

## Propriedades {#id-properties}

Sequência de texto. Obrigatório. Chave de índice primária para a tabela de dados da imagem. Cada valor de catalog::Id deve ser exclusivo na tabela.

## Padrão {#id-default}

Nenhum.

## Consulte também {#id-seealso}

[atributo::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
