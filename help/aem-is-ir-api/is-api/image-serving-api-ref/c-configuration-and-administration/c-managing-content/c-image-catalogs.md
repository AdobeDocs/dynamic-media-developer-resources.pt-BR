---
description: Os catálogos de imagens fornecem várias configurações do servidor, além de fontes, perfis ICC e macros de comando.
seo-description: Os catálogos de imagens fornecem várias configurações do servidor, além de fontes, perfis ICC e macros de comando.
seo-title: Catálogos de imagens
solution: Experience Manager
title: Catálogos de imagens
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7d7285e2-ee9c-4e88-b270-b686d1984d82
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# Catálogos de imagem{#image-catalogs}

Os catálogos de imagens fornecem várias configurações do servidor, além de fontes, perfis ICC e macros de comando.

Eles mapeiam IDs de imagem e conteúdo estático usadas em solicitações para caminhos de arquivo reais, armazenam vários metadados de imagem, como mapas de imagem, e fornecem container para modelos e conjuntos de imagens.

Os catálogos de imagens são acessados somente pelo Servidor de plataforma, nunca pelo Servidor de imagens. Os arquivos de atributos do catálogo devem ter um sufixo .ini e ser colocados na pasta de catálogo do Servidor de plataforma ( `PS::CatalogFolder`). Pelo menos o catálogo de imagem padrão é obrigatório e deve ser preenchido com todos os atributos para o funcionamento correto do Servidor de plataforma.
