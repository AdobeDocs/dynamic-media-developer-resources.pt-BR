---
description: Cadeia modificadora de solicitação de prefixo. Nenhum ou mais comandos do Servidor de imagens separados por caracteres '&'.
solution: Experience Manager
title: Modificador
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6eef3159-c082-469b-b9dc-29acb28560d6
TQID: 'https://experienceleague.adobe.com/b1j5WmY-PNOt1zW9qglJob5W8csmI3TidhDwoHK3kCM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 0%

---

# Modificador{#modifier}

Cadeia modificadora de solicitação de prefixo. Nenhum ou mais comandos do Servidor de imagens separados por caracteres &#39;&amp;&#39;.

Usado para modificar persistentemente imagens e armazenar o corpo de modelos.

Os comandos neste campo são substituídos pelos mesmos comandos na solicitação ou no modelo do qual esse registro é referenciado e pelos comandos em `catalog::PostModifier`

As macros são permitidas em `catalog::Modifier`, desde que estejam definidas no mesmo catálogo ou no catálogo padrão. Variáveis personalizadas também podem ser usadas.

## Propriedades {#section-6674388f77d644469371a17e8809c45f}

String de texto. Opcional.

## Padrão {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Nenhum.

## Consulte também {#section-7a67803d141b442180c418c1f3cff029}

[catálogo::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
