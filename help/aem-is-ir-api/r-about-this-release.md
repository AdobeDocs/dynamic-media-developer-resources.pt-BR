---
description: Esta versão — Image Serving 6.6.1 e Image Rendering 6.6.1 — substitui o Image Serving 6.5.3 e o Image Rendering 6.5.3.
seo-description: Esta versão — Image Serving 6.6.1 e Image Rendering 6.6.1 — substitui o Image Serving 6.5.3 e o Image Rendering 6.5.3.
seo-title: Sobre esta versão
solution: Experience Manager
title: Sobre esta versão
uuid: 2fdd8920-433b-405e-bf93-dbef5735be3f
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Sobre esta versão{#about-this-release}

Esta versão — Image Serving 6.6.1 e Image Rendering 6.6.1 — substitui o Image Serving 6.5.3 e o Image Rendering 6.5.3.

## Problemas conhecidos e alterações de comportamento {#section-9dbc05206187477f926a78e8108a34e1}

* O uso do caractere de ponto de interrogação nas IDs de ativo não é mais suportado, mesmo se o caractere for codificado no URL.
* As solicitações de banner dinâmico `/xfl/flash/` não são mais suportadas e agora retornam um código de erro http 404.
* As solicitações W2P `/is/agm/` não são mais suportadas.
* Algumas mensagens de erro não são mais renderizadas no navegador. Dessa forma, é necessário revisar o log de rastreamento para depurar.

## Novos recursos {#section-b1386e36cb4544ebb79766a06b16842d}

* Amostra inteligente
* Corte inteligente

## Correção de erros {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Correção de um problema em que a opção `\qc` RTF seguida por um espaço fazia com que uma solicitação não fosse renderizada.

