---
description: As camadas são compostas na ordem especificada pelo comando layer=, onde as camadas com numeração mais alta ocultam as com numeração mais baixa.
seo-description: As camadas são compostas na ordem especificada pelo comando layer=, onde as camadas com numeração mais alta ocultam as com numeração mais baixa.
seo-title: A tela de composição
solution: Experience Manager
title: A tela de composição
topic: Scene7 Image Serving - Image Rendering API
uuid: 057b11cb-36f3-40f8-b095-9ad05da858a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# A tela de composição{#the-compositing-canvas}

As camadas são compostas na ordem especificada pelo comando layer=, onde as camadas com numeração mais alta ocultam as com numeração mais baixa.

A camada 0 constitui a camada de plano de fundo, que é sempre necessária e que define o tamanho da imagem composta. Qualquer um dos tipos de camada é permitido para a camada 0. O tamanho da camada 0 deve ser definido, usando explicitamente `size=` ou implicitamente, com base na imagem ou no texto do conteúdo. Quaisquer áreas de outras camadas que não se encaixem na área da camada 0 não serão incluídas na imagem de saída.

>[!NOTE] {class=&quot;- tópico/observação &quot;}
>
>Depois que todas as camadas são niveladas, a imagem composta é convertida na imagem de resposta final, conforme especificado com os comandos e atributos [da](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)visualização.

