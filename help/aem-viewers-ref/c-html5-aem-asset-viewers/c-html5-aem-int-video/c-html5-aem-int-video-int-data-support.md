---
title: Suporte a dados interativos
description: O Visualizador de vídeo interativo é compatível com a renderização de amostras interativas com base em dados interativos passados para o visualizador como um parâmetro de configuração.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
TQID: 'https://experienceleague.adobe.com/HE4LeluT9FWi8xgQf259b1yakK0oQjeR3rDME0juZiU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 223
ht-degree: 0%

---

# Suporte a dados interativos{#interactive-data-support}

O Visualizador de vídeo interativo é compatível com a renderização de amostras interativas com base em dados interativos passados para o visualizador como um parâmetro de configuração.

A amostra visível no momento corresponde à região de tempo do vídeo à qual ela está associada. Clicar ou tocar na amostra interativa aciona a ação atribuída a ela no momento da criação.

A amostra interativa pode ativar uma Visualização rápida na página da Web de hospedagem acionando um retorno de chamada do JavaScript ou pode redirecionar o usuário para uma página da Web externa.

## Sobre o Quickview {#section-7990e44f641042d2a38ba20c9413b3f8}

Esses tipos de amostras interativas devem ser criadas usando o tipo de ação &quot;quickview&quot; no Adobe Experience Manager Assets - On-demand. Quando um usuário ativa essa amostra, o visualizador executa o retorno de chamada do JavaScript `quickViewActivate` e passa os dados da amostra para ele. Espera-se que a página da Web que incorpora o escute essa chamada de retorno e, quando ela é acionada, a página abre sua própria implementação do Quickview.

## Redirecionar para uma página externa da Web {#section-32ebe3c3a7f74892a428c5d48801de4d}

Amostras criadas para o tipo de ação &quot;visualização rápida&quot; no Experience Manager Assets - o redirecionamento sob demanda do usuário para um URL externo. Dependendo das configurações no momento da criação, o URL pode ser aberto em uma nova guia do navegador, na mesma janela ou na janela do navegador nomeada.
