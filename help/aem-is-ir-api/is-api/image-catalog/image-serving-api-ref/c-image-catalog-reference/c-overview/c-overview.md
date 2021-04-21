---
description: Os catálogos de imagens são usados para fornecer informações sobre imagens e dados de suporte (como fontes e perfis ICC) ao servidor.
solution: Experience Manager
title: Visão geral
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---


# Visão geral{#overview}

Os catálogos de imagens são usados para fornecer informações sobre imagens e dados de suporte (como fontes e perfis ICC) ao servidor.

Os catálogos de imagens são usados para fornecer informações sobre imagens e dados de suporte (como fontes e perfis ICC) ao servidor.

Cada catálogo de imagens consiste em um arquivo de atributo de catálogo necessário e um conjunto de arquivos de dados de catálogo opcionais:

* O arquivo de dados da imagem, que classifica imagens e modelos e seus metadados associados.
* O arquivo de dados SVG, que classifica arquivos SVG e seus metadados associados.
* O arquivo de definições de macro, que fornece definições para macros de solicitação.
* O arquivo do mapa de fontes, que mantém o controle das fontes de texto.
* O arquivo de mapa de perfil, que discrimina perfis de cores ICC.
* O arquivo do conjunto de regras, que define as regras de pré-processamento da solicitação HTTP.

Os arquivos de dados do catálogo são associados a catálogos de imagens por referências de arquivo no arquivo de atributo do catálogo. O mesmo arquivo de dados de catálogo pode ser compartilhado por vários catálogos de imagens.

Os arquivos de atributos do catálogo devem ter um sufixo de arquivo [!DNL .ini] e devem estar localizados na pasta de catálogo do Servidor de Plataforma ( `PlatformServer::catalog.rootPath`). Os arquivos de dados do catálogo podem ser localizados na mesma pasta ou em qualquer outra pasta acessível ao Servidor de plataforma.

Este documento descreve o formato de arquivo do Catálogo de Imagens para o sistema Dynamic Media Image Serving. O público-alvo é programadores experientes e desenvolvedores de sites que desejam utilizar o Dynamic Media Image Serving para um aplicativo da Web ou personalizado.

Pressupõe-se que o leitor esteja familiarizado com o sistema Dynamic Media Image Serving, padrões e convenções gerais de protocolo HTTP e terminologia básica de geração de imagens.
