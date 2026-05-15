---
title: pathEmbed
description: Incorporar dados de caminhos. Especifica se os caminhos de Photoshop do arquivo de imagem de origem da camada 0 devem ser incluídos na imagem de resposta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
TQID: 'https://experienceleague.adobe.com/ES7nAoYjO6Y4naU2c5TIPotPUTjncwjRMLL7-4--XpE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 0%

---

# pathEmbed{#pathembed}

Incorporar dados de caminhos. Especifica se os caminhos de Photoshop do arquivo de imagem de origem da camada 0 devem ser incluídos na imagem de resposta.

`pathEmbed=0|1`

## Propriedades {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Solicitar atributo. Ignorado se a imagem de origem não contiver dados de caminhos. Os dados dos caminhos são dimensionados e girados como os dados da imagem. Somente caminhos da imagem de origem de `layer=0` são processados; caminhos de outras imagens de camada são ignorados.

Ignorado se o formato de imagem de saída não suportar incorporação de caminho. Consulte a descrição de `fmt=` para obter uma lista de formatos de imagem de saída que oferecem suporte à incorporação de caminhos.

## Restrições {#section-697cddb79a1542bc8457d2f4f59eec69}

Caminhos abertos do Photoshop (caminhos que não formam loops fechados) não são compatíveis com a incorporação na imagem de resposta no momento.

## Padrão {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, para nenhuma incorporação de caminhos em imagens de saída.

## Consulte também {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
