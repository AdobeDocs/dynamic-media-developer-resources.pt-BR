---
description: Id
solution: Experience Manager
title: Id
topic: Scene7 Image Serving - Image Rendering API
uuid: a700472c-e1eb-4eb0-95ff-7afd4ce27931
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Id{#id}

Geralmente, um identificador curto e exclusivo, como um número SKU, possivelmente com algum tipo de sufixo, como se um SKU tem várias imagens ou variações específicas de localidade. Pode também ser uma sequência de caracteres mais complexa, mais parecida com um caminho de arquivo, para suportar a fácil adaptação de sites com o Serviço de imagem.

>[!NOTE]
>
>As tabelas image e SVG são mescladas em uma única tabela quando o catálogo de imagens é carregado. Os valores de ID devem ser exclusivos em ambas as tabelas. O registro SVG será descartado se a tabela de imagem contiver um registro com o mesmo valor de ID. O conteúdo estático é gerido com uma tabela separada; itens de conteúdo estático e itens de imagem/SVG podem, portanto, ter os mesmos valores de Id.

## Propriedades {#section-874a6853f67b4b229341ca76682884ae}

Sequência de caracteres de texto. Obrigatório. Identificador de registro para a imagem/SVG ou tabela de dados de conteúdo estático. Cada valor `catalog::Id` neste catálogo de imagens/catálogo SVG ou neste catálogo de conteúdo estático deve ser exclusivo e não deve incluir caracteres &#39;,&#39;.

## Padrão {#section-a26e7d83a5ee44b5918baef82ee48e14}

Nenhum.

## Consulte também {#section-a258d818487d4ee6b7a99a65d18471a9}

[atributo::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
