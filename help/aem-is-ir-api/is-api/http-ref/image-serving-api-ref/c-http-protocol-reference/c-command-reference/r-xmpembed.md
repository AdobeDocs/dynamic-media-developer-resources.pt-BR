---
title: xmpEmbed
description: Incorporar metadados do XMP. Especifica se os metadados do XMP devem ser incluídos na imagem de resposta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
TQID: 'https://experienceleague.adobe.com/2pISbWU-Y-4szY0jmZswDIxvBrPlJ1yZmQby0sZ1v-o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 0%

---

# xmpEmbed{#xmpembed}

Incorporar metadados do XMP. Especifica se os metadados do XMP devem ser incluídos na imagem de resposta.

`xmpEmbed=0|1`

>[!NOTE]
>
>Os dados do XMP são passados da imagem de origem para a imagem de resposta sem modificação. Isso pode resultar na incorporação de dados incorretos na imagem de resposta.

## Propriedades {#section-27024c4272f44d9a8c264a0629193af2}

Solicitar atributo. Ignorado se a imagem de origem não contiver dados do XMP. Somente dados XMP da imagem de origem de `layer=0` são processados. Os dados do XMP de outras imagens de camada são ignorados.

Ignorado se o formato da imagem de saída não suportar a incorporação do XMP. Consulte a descrição de `fmt=` para obter uma lista de formatos de imagem de saída que oferecem suporte à incorporação do XMP.

## Padrão {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, para nenhuma incorporação de caminhos em imagens de saída.

## Consulte também {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
