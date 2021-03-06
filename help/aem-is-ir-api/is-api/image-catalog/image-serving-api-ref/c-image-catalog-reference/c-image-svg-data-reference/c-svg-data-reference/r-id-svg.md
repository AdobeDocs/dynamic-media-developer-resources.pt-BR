---
description: Id
solution: Experience Manager
title: Id
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: d7b37180-cc93-41cd-bf14-5c262b046fbc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# Id{#id}

Normalmente, é um identificador curto e exclusivo, como um número SKU, possivelmente com algum tipo de sufixo, como se um SKU tiver várias imagens ou variações específicas da localidade. Pode também ser uma sequência de caracteres mais complexa, mais parecida com um caminho de arquivo, para suportar a fácil remontagem de sites com o Serviço de imagem.

>[!NOTE]
>
>As tabelas de imagem e SVG são mescladas em uma única tabela quando o catálogo de imagem é carregado. Os valores de ID devem ser exclusivos em ambas as tabelas. O registro SVG será descartado se a tabela de imagem contiver um registro com o mesmo valor de ID. O conteúdo estático é gerenciado com uma tabela separada; itens de conteúdo estático e itens de imagem/SVG podem ter os mesmos valores de ID.

## Propriedades {#section-874a6853f67b4b229341ca76682884ae}

Sequência de texto. Obrigatório. Identificador de registro para a imagem/SVG ou tabela de dados de conteúdo estático. Cada valor `catalog::Id` neste catálogo de imagens/SVG ou neste catálogo de conteúdo estático deve ser exclusivo e não deve incluir caracteres &#39;,&#39;.

## Padrão {#section-a26e7d83a5ee44b5918baef82ee48e14}

Nenhum.

## Consulte também {#section-a258d818487d4ee6b7a99a65d18471a9}

[atributo::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
