---
description: Os catálogos de imagens são usados para fornecer informações sobre imagens e dados de suporte (como fontes e perfis ICC) ao servidor.
seo-description: Os catálogos de imagens são usados para fornecer informações sobre imagens e dados de suporte (como fontes e perfis ICC) ao servidor.
seo-title: Visão geral
solution: Experience Manager
title: Visão geral
topic: Scene7 Image Serving - Image Rendering API
uuid: e8c0401b-9161-4624-babb-6c7afb443e65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Visão geral{#overview}

Os catálogos de imagens são usados para fornecer informações sobre imagens e dados de suporte (como fontes e perfis ICC) ao servidor.

Os catálogos de imagens são usados para fornecer informações sobre imagens e dados de suporte (como fontes e perfis ICC) ao servidor.

Cada catálogo de imagens consiste em um arquivo de atributo de catálogo necessário e um conjunto de arquivos de dados de catálogo opcionais:

* O arquivo de dados da imagem, que classifica imagens e modelos e seus metadados associados.
* O arquivo de dados SVG, que classifica os arquivos SVG e seus metadados associados.
* O arquivo de definições de macro, que fornece definições para macros de solicitação.
* O arquivo de mapa de fontes, que monitora as fontes de texto.
* O arquivo de mapa de perfis, que simboliza perfis de cores ICC.
* O arquivo de conjunto de regras, que define as regras de pré-processamento da solicitação HTTP.

Os arquivos de dados do catálogo são associados aos catálogos de imagens por referências de arquivo no arquivo de atributos do catálogo. O mesmo arquivo de dados do catálogo pode ser compartilhado por vários catálogos de imagens.

Os arquivos de atributo do catálogo devem ter um sufixo de [!DNL .ini] arquivo e devem estar localizados na pasta de catálogo do Servidor de plataforma ( `PlatformServer::catalog.rootPath`). Os arquivos de dados do catálogo podem ser localizados na mesma pasta ou em qualquer outra pasta acessível ao Servidor da plataforma.

Este documento descreve o formato de arquivo do Catálogo de imagens para o sistema Scene7 Image Serving. A audiência pretendida é programadores experientes e desenvolvedores de sites da Web que desejam utilizar o Scene7 Image Serving para uma aplicação Web ou personalizada.

Pressupõe-se que o leitor esteja familiarizado com o sistema Scene7 Image Serving, padrões e convenções gerais de protocolo HTTP e terminologia básica de geração de imagens.
