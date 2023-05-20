---
title: pathEmbed
description: Incorporar dados de caminhos. Especifica se os caminhos Photoshop inseridos na vinheta devem ser incluídos na imagem de resposta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 66cc57ef-964e-4062-bb66-efeda15be744
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# pathEmbed{#pathembed}

Incorporar dados de caminhos. Especifica se os caminhos Photoshop inseridos na vinheta devem ser incluídos na imagem de resposta.

`pathEmbed=0|1`

## Propriedades {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Solicitar atributo. Ignorado se a vinheta não contiver dados de caminhos. Os dados de caminhos são dimensionados para `wid=` e/ou `hei=` se necessário.

Ignorado se o formato de imagem de saída não suportar incorporação de caminho. Consulte a descrição de `fmt=` para obter uma lista de formatos de imagem de saída que oferecem suporte à incorporação de caminhos.

## Padrão {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, para nenhuma incorporação de caminhos em imagens de saída.

## Consulte também {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
