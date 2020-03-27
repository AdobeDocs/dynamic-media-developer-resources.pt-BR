---
description: Os catálogos de imagens fornecem várias configurações do servidor, além de fontes, perfis ICC e macros de comando.
seo-description: Os catálogos de imagens fornecem várias configurações do servidor, além de fontes, perfis ICC e macros de comando.
seo-title: Catálogos de imagens
solution: Experience Manager
title: Catálogos de imagens
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d7285e2-ee9c-4e88-b270-b686d1984d82
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Catálogos de imagens{#image-catalogs}

Os catálogos de imagens fornecem várias configurações do servidor, além de fontes, perfis ICC e macros de comando.

Eles mapeiam IDs de imagem e conteúdo estático usadas em solicitações para caminhos de arquivo reais, armazenam vários metadados de imagem, como mapas de imagem, e fornecem container para modelos e conjuntos de imagens.

Os catálogos de imagens são acessados apenas pelo Servidor de plataforma, nunca pelo Servidor de imagens. Os arquivos de atributos do catálogo devem ter um sufixo .ini e ser colocados na pasta de catálogo do Servidor de plataforma ( `PS::CatalogFolder`). Pelo menos o catálogo de imagem padrão é obrigatório e deve ser preenchido com todos os atributos para o funcionamento correto do Servidor de plataforma.
