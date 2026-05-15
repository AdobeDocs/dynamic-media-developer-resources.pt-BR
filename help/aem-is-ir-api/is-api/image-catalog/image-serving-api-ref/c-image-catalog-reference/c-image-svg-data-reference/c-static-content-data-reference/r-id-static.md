---
title: ID
description: Normalmente, um identificador curto e exclusivo, como um número SKU, possivelmente com algum tipo de sufixo, como se um SKU tivesse várias imagens ou variações específicas de localidade.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
TQID: 'https://experienceleague.adobe.com/xPBbjaHO58J-4HFnChD1ybEVoE2AbRZuFVA8nbquEvg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 0%

---

# ID{#id}

Normalmente, um identificador curto e exclusivo, como um número SKU, possivelmente com algum tipo de sufixo, como se um SKU tiver várias imagens ou variações específicas de localidade. Também pode ser uma sequência de caracteres mais complexa, que se parece mais com um caminho de arquivo, para oferecer suporte à fácil adaptação de sites com o Servidor de imagens.

>[!NOTE]
>
>As tabelas de imagem e SVG são mescladas em uma única tabela quando o catálogo de imagens é carregado. Os valores de ID devem ser exclusivos em ambas as tabelas. O registro SVG é descartado se a tabela de imagens contiver um registro com o mesmo valor de ID. O conteúdo estático é gerenciado com uma tabela separada; os itens de conteúdo estático e os itens de imagem/SVG podem ter os mesmos valores de ID.

## Propriedades {#section-874a6853f67b4b229341ca76682884ae}

String de texto. Obrigatório. Identificador de registro para a imagem/SVG ou tabela de dados de conteúdo estático. Cada valor `catalog::Id` nesse catálogo de imagens/catálogo SVG ou nesse catálogo de conteúdo estático deve ser exclusivo e não deve incluir caracteres &#39;,&#39;.

## Padrão {#section-a26e7d83a5ee44b5918baef82ee48e14}

Nenhum.

## Consulte também {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
