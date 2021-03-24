---
description: Os catálogos de imagens fornecem muitas configurações do servidor, assim como fontes, perfis ICC, macros de comando.
solution: Experience Manager
title: Catálogos de imagens
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# Catálogos de imagem{#image-catalogs}

Os catálogos de imagens fornecem muitas configurações do servidor, assim como fontes, perfis ICC, macros de comando.

Eles mapeiam ids de imagem e conteúdo estático usadas em solicitações para caminhos de arquivo reais, armazenam vários metadados de imagem, como mapas de imagem, e fornecem contêineres para modelos e conjuntos de imagens.

Os catálogos de imagem são acessados somente pelo Servidor de plataforma, nunca pelo Servidor de imagem. Os arquivos de atributo do catálogo devem ter um sufixo .ini e ser colocados na pasta de catálogo do Servidor de plataforma ( `PS::CatalogFolder`). Pelo menos o catálogo de imagem padrão é necessário e deve ser preenchido com todos os atributos para o funcionamento correto do Servidor de plataforma.
