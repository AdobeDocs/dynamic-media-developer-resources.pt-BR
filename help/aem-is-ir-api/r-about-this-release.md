---
description: Esta versão (Servidor de imagens 6.6.1 e Renderização de imagem 6.6.1) substitui o Servidor de imagens 6.5.3 e a Renderização de imagem 6.5.3.
solution: Experience Manager
title: Sobre esta versão
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Sobre esta versão{#about-this-release}

Esta versão (Servidor de imagens 6.6.1 e Renderização de imagem 6.6.1) substitui o Servidor de imagens 6.5.3 e a Renderização de imagem 6.5.3.

## Problemas conhecidos e alterações de comportamento {#section-9dbc05206187477f926a78e8108a34e1}

* O uso do caractere de ponto de interrogação nas IDs de ativos não é mais suportado, mesmo que o caractere esteja codificado no URL.
* Banner dinâmico `/xfl/flash/` As solicitações do não são mais suportadas e agora retornam um código de erro HTTP 404.
* W2P `/is/agm/` As solicitações do não são mais compatíveis.
* Algumas mensagens de erro não são mais renderizadas para o navegador. Dessa forma, você precisa revisar o log de rastreamento para depurar.

## Novos recursos {#section-b1386e36cb4544ebb79766a06b16842d}

* Amostra inteligente
* Corte inteligente

## Correção de erros {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Correção de um problema em que `\qc` A opção RTF seguida por um espaço fez com que uma solicitação não fosse renderizada.
