---
description: O Visualizador de vídeo interativo suporta a renderização de amostras interativas com base em dados interativos passados ao visualizador como um parâmetro de configuração.
seo-description: O Visualizador de vídeo interativo suporta a renderização de amostras interativas com base em dados interativos passados ao visualizador como um parâmetro de configuração.
seo-title: Suporte a dados interativos
solution: Experience Manager
title: Suporte a dados interativos
uuid: 70b2ec2e-0ea7-461d-a185-731fb0ef8f3e
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---


# Suporte a dados interativos{#interactive-data-support}

O Visualizador de vídeo interativo suporta a renderização de amostras interativas com base em dados interativos passados ao visualizador como um parâmetro de configuração.

A amostra atualmente visível corresponde à região de tempo do vídeo à qual está associada. Clicar ou tocar na amostra interativa aciona a ação atribuída a ela no momento do autor.

A amostra interativa pode ativar uma Exibição rápida na página da Web de hospedagem, acionando um retorno de chamada JavaScript ou pode redirecionar o usuário para uma página da Web externa.

## Sobre a Exibição Rápida {#section-7990e44f641042d2a38ba20c9413b3f8}

Esses tipos de amostras interativas devem ser criadas usando o tipo de ação &quot;quickview&quot; no AEM Assets - sob demanda. Quando um usuário ativa essa amostra, o visualizador executa `quickViewActivate` o retorno de chamada do JavaScript e transmite os dados da amostra para ele. Espera-se que a página da Web de incorporação escute essa chamada de retorno e, quando aciona, a página abre sua própria implementação da Exibição rápida.

## Redirecionar para uma página da Web externa {#section-32ebe3c3a7f74892a428c5d48801de4d}

Amostras criadas para o tipo de ação &quot;quickview&quot; no AEM Assets - redirecionam o usuário sob demanda para um URL externo. Dependendo das configurações no momento da criação, o URL pode abrir em uma nova guia do navegador, na mesma janela ou na janela do navegador nomeado.
