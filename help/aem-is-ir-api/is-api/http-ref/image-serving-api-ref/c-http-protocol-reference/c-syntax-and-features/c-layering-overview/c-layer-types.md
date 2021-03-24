---
description: Há suporte para quatro tipos de camadas.
solution: Experience Manager
title: Tipos de camada
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---


# Tipos de camada{#layer-types}

Há suporte para quatro tipos de camadas.

## Camadas de imagem {#section-3e53df1437694272aca03f927fc0db07}

As camadas de imagem devem ter um comando `src=` que especifica a imagem a ser usada como a camada. Uma imagem separada pode ser especificada com `mask=` para ser usada como máscara de camada ou a imagem já pode ter um canal alfa. O tamanho das camadas de imagem é sempre derivado da imagem, mas a imagem geralmente é dimensionada para se ajustar usando o comando `size=`. Um caminho de clipe pode ser aplicado com `clipPath=`.

## Camadas de texto {#section-dc2aec6416a340bcb20c1f884323c8d0}

Deve ter um comando `text=` ou `textPs=` que forneça o conteúdo do texto na forma de um fragmento de texto formatado de rich text (RTF). As camadas de texto podem ser de autodimensionamento para o conteúdo ou podem receber tamanhos explícitos (por exemplo, se o texto deve ser vinculado a uma largura específica ou se o texto deve ser restrito em uma área específica). `textPs=` suporte o fluxo de texto em formas arbitrárias definidas com  `textFlowPath=` e em caminhos arbitrários definidos com  `textPath=`. `textPs=` também suporta a renderização de texto na caixa de texto ou na forma especificada em ângulos arbitrários (  `textAngle=`).

## Camadas de cor sólida {#section-56dfb672756643dda08dc93294809eb0}

As camadas de cores sólidas geralmente são usadas para a camada 0 em modelos, de modo que o tamanho da imagem composta é fixo e independente de qualquer conteúdo de imagem. As camadas de cores sólidas exigem um atributo `color=` e `size=` ou `mask=`, além de terem suporte para a maioria dos outros comandos e atributos para modificar a aparência. As camadas de cores sólidas podem receber formas arbitrárias com `clipPath=`.

## Camadas de efeito {#section-dd3b628bc6734077af4c0ddcebcee05f}

Os efeitos de camada de estilo Photoshop, como sombras de soltar e efeitos de brilho, são implementados pelo IS usando subcamadas especiais que podem ser anexadas a camadas de imagem, texto e cor sólida. Essas camadas de efeito herdam a máscara de camada pai e a posição da camada pai e são limitadas na funcionalidade.
