---
description: Esta versão (Servidor de imagens 6.6.1 e Renderização de imagem 6.6.1) substitui o Servidor de imagens 6.5.3 e a Renderização de imagem 6.5.3.
solution: Experience Manager
title: Sobre esta versão
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
TQID: 'https://experienceleague.adobe.com/Mv84kHB7jsBYAvY1j--l8Ly5VZtKwFq-SsNdz2TIQOE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 0%

---

# Sobre esta versão{#about-this-release}

Esta versão (Servidor de imagens 6.6.1 e Renderização de imagem 6.6.1) substitui o Servidor de imagens 6.5.3 e a Renderização de imagem 6.5.3.

## Problemas conhecidos e alterações de comportamento {#section-9dbc05206187477f926a78e8108a34e1}

* O uso do caractere de ponto de interrogação nas IDs de ativos não é mais suportado, mesmo que o caractere esteja codificado no URL.
* As solicitações de banner dinâmico `/xfl/flash/` não são mais suportadas e agora retornam um código de erro HTTP 404.
* Não há mais suporte para solicitações `/is/agm/` W2P.
* Algumas mensagens de erro não são mais renderizadas para o navegador. Dessa forma, você precisa revisar o log de rastreamento para depurar.

## Novos recursos {#section-b1386e36cb4544ebb79766a06b16842d}

* Amostra inteligente
* Corte inteligente

## Correção de erros {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Correção de um problema em que a opção RTF `\qc` seguida de um espaço fazia com que uma solicitação não fosse renderizada.
