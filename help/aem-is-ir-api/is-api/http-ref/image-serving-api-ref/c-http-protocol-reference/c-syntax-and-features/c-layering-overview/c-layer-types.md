---
description: Há suporte para quatro tipos de camadas.
solution: Experience Manager
title: Tipos de camada
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Tipos de camada{#layer-types}

Há suporte para quatro tipos de camadas.

## Camadas de imagem {#section-3e53df1437694272aca03f927fc0db07}

As camadas de imagem devem ter uma `src=` comando que especifica a imagem a ser usada como a camada. Uma imagem separada pode ser especificada com `mask=` para ser usada como máscara de camada ou a imagem pode já ter um canal alfa. O tamanho das camadas de imagem é sempre derivado da imagem, mas a imagem geralmente é dimensionada para caber usando o `size=` comando. Um caminho de clipe pode ser aplicado com `clipPath=`.

## Camadas de texto {#section-dc2aec6416a340bcb20c1f884323c8d0}

Deve ter um `text=` ou `textPs=` comando que fornece o conteúdo do texto na forma de um fragmento de texto RTF (rich text-formatted). As camadas de texto podem ser autodimensionáveis para seu conteúdo ou podem receber tamanhos explícitos (por exemplo, se o texto deve ser ajustado para uma largura específica ou se o texto deve ser restrito dentro de uma área específica). `textPs=` suporte ao fluxo de texto em formas arbitrárias definidas com `textFlowPath=` e em caminhos arbitrários definidos com `textPath=`. `textPs=` O também oferece suporte para a renderização de texto na caixa de texto ou forma especificada em ângulos arbitrários ( `textAngle=`).

## Camadas de cores sólidas {#section-56dfb672756643dda08dc93294809eb0}

Camadas de cores sólidas geralmente são usadas para a camada 0 em modelos, de modo que o tamanho da imagem composta seja fixo e independente de qualquer conteúdo de imagem. Camadas de cores sólidas exigem um `color=` atributo, e `size=` ou `mask=`e oferecem suporte para a maioria dos outros comandos e atributos para modificar a aparência. Camadas de cores sólidas podem receber formas arbitrárias com `clipPath=`.

## Camadas de efeito {#section-dd3b628bc6734077af4c0ddcebcee05f}

Os efeitos de camada do estilo Photoshop, como sombras projetadas e efeitos de brilho, são implementados pelo IS usando subcamadas especiais que podem ser anexadas a camadas de imagem, texto e cores sólidas. Essas camadas de efeito herdam a máscara e a posição da camada pai e têm funcionalidade limitada.
