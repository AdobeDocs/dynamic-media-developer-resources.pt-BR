---
description: Os catálogos de imagens são usados para fornecer informações sobre imagens e dados de suporte (como fontes e perfis ICC) ao servidor.
solution: Experience Manager
title: Visão geral
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Visão geral{#overview}

Os catálogos de imagens são usados para fornecer informações sobre imagens e dados de suporte (como fontes e perfis ICC) ao servidor.

Os catálogos de imagens são usados para fornecer informações sobre imagens e dados de suporte (como fontes e perfis ICC) ao servidor.

Cada catálogo de imagens consiste em um arquivo de atributo de catálogo necessário e um conjunto de arquivos de dados de catálogo opcionais:

* O arquivo de dados de imagem, que relaciona imagens e modelos e seus metadados associados.
* O arquivo de dados do SVG, que apresenta os arquivos SVG e seus metadados associados.
* O arquivo de definições de macro, que fornece definições para macros de solicitação.
* O arquivo do mapa de fontes, que controla as fontes de texto.
* O arquivo do mapa de perfis, que apresenta os perfis de cores do ICC.
* O arquivo de conjunto de regras, que define as regras de pré-processamento da solicitação HTTP.

Os arquivos de dados de catálogo são associados aos catálogos de imagem por referências de arquivo no arquivo de atributo de catálogo. O mesmo arquivo de dados de catálogo pode ser compartilhado por vários catálogos de imagem.

Os arquivos de atributo de catálogo devem ter um sufixo de arquivo [!DNL .ini] e devem estar localizados na pasta de catálogo de [!DNL Platform Server] ( `PlatformServer::catalog.rootPath`). Os arquivos de dados do catálogo podem estar localizados na mesma pasta ou em qualquer outra pasta acessível ao [!DNL Platform Server].

Este documento descreve o formato de arquivo do Catálogo de imagens para o sistema de disponibilização de imagens do Dynamic Media. O público-alvo é de programadores experientes e desenvolvedores de sites que desejam aproveitar o Servidor de imagens do Dynamic Media para um aplicativo da Web ou personalizado.

Presume-se que o leitor esteja familiarizado com o sistema de disponibilização de imagens do Dynamic Media, padrões e convenções gerais do protocolo HTTP e terminologia básica de geração de imagens.
