---
description: Identificador do registro de catálogo
solution: Experience Manager
title: Id
uuid: 9803d754-1f94-4e5d-9a40-3936676c0035
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
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