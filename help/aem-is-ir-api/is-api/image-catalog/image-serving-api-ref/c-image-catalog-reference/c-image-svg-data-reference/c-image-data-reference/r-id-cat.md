---
description: Identificador de registro do catálogo
solution: Experience Manager
title: ID
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# ID {#id}

O valor da chave de índice pelo qual os registros no arquivo de dados de imagem são pesquisados pelo [!DNL Platform Server].

Normalmente, um identificador de imagem curto e exclusivo, como um número SKU, possivelmente com algum tipo de sufixo de imagem, se um SKU tiver várias imagens. Também pode ser uma sequência de caracteres mais complexa que se parece mais com um caminho de arquivo, para suportar o redirecionamento fácil de sites com o Servidor de imagens.

## Propriedades {#id-properties}

String de texto. Obrigatório. Chave de índice principal da tabela de dados de imagem. Cada valor catalog::Id deve ser exclusivo na tabela.

## Padrão {#id-default}

Nenhum.

## Consulte também {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
