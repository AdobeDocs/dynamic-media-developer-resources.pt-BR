---
title: pathEmbed
description: Incorporar dados de caminhos. Especifica se os caminhos Photoshop inseridos na vinheta devem ser incluídos na imagem de resposta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 66cc57ef-964e-4062-bb66-efeda15be744
TQID: 'https://experienceleague.adobe.com/WRh7noh5vPtAHpz58VbzUB9nqLqQmGBUTW9PCG-RrtU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 0%

---

# pathEmbed{#pathembed}

Incorporar dados de caminhos. Especifica se os caminhos Photoshop inseridos na vinheta devem ser incluídos na imagem de resposta.

`pathEmbed=0|1`

## Propriedades {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Solicitar atributo. Ignorado se a vinheta não contiver dados de caminhos. Os dados dos caminhos são dimensionados para `wid=` e/ou `hei=` se necessário.

Ignorado se o formato de imagem de saída não suportar incorporação de caminho. Consulte a descrição de `fmt=` para obter uma lista de formatos de imagem de saída que oferecem suporte à incorporação de caminhos.

## Padrão {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, para nenhuma incorporação de caminhos em imagens de saída.

## Consulte também {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
