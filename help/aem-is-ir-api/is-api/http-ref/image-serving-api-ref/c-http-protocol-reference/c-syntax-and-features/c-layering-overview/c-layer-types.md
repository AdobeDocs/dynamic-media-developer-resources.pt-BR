---
description: Há suporte para quatro tipos de camadas.
seo-description: Há suporte para quatro tipos de camadas.
seo-title: Tipos de camada
solution: Experience Manager
title: Tipos de camada
topic: Scene7 Image Serving - Image Rendering API
uuid: d88b2163-7c9f-4885-9722-be3339e7127a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Tipos de camada{#layer-types}

Há suporte para quatro tipos de camadas.

## Camadas de imagem {#section-3e53df1437694272aca03f927fc0db07}

As camadas de imagem devem ter um `src=` comando que especifique a imagem a ser usada como camada. Uma imagem separada pode ser especificada com `mask=` o objetivo de ser usada como máscara de camada ou a imagem pode já ter um canal alfa. O tamanho das camadas de imagem é sempre derivado da imagem, mas a imagem geralmente é dimensionada para se ajustar usando o `size=` comando. Um caminho de clipe pode ser aplicado com `clipPath=`.

## Camadas de texto {#section-dc2aec6416a340bcb20c1f884323c8d0}

Deve ter um comando `text=` ou `textPs=` que forneça o conteúdo do texto na forma de um fragmento de texto formatado em RTF (Rich Text-Forted). As camadas de texto podem ser autodimensionadas para seu conteúdo ou podem receber tamanhos explícitos (por exemplo, se o texto deve ser vinculado a uma largura específica ou se o texto deve ser restrito em uma área específica). `textPs=` suporte o fluxo de texto em formas arbitrárias definidas com `textFlowPath=` e em caminhos arbitrários definidos com `textPath=`. `textPs=` também suporta a renderização de texto na caixa de texto ou na forma especificada em ângulos arbitrários ( `textAngle=`).

## Camadas de cor sólida {#section-56dfb672756643dda08dc93294809eb0}

As camadas de cor sólida são frequentemente usadas para a camada 0 em modelos, de modo que o tamanho da imagem composta seja fixo e independente de qualquer conteúdo de imagem. As camadas de cores sólidas exigem um `color=` atributo, `size=` ou `mask=`, e suportam a maioria dos outros comandos e atributos para modificar a aparência. As camadas de cor sólida podem receber formas arbitrárias com `clipPath=`.

## Camadas de efeito {#section-dd3b628bc6734077af4c0ddcebcee05f}

Os efeitos de camada estilo Photoshop, como sombras projetadas e efeitos de brilho, são implementados pelo IS usando subcamadas especiais que podem ser anexadas a camadas de imagem, texto e cores sólidas. Essas camadas de efeito herdam a máscara de camada pai e a posição da camada pai e são limitadas na funcionalidade.
