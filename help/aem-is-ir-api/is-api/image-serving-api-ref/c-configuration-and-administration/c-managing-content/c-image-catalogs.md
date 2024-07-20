---
description: Os catálogos de imagens fornecem muitas definições de configuração do servidor, assim como fontes, perfis ICC e macros de comandos.
solution: Experience Manager
title: Catálogos de imagens
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Catálogos de imagens{#image-catalogs}

Os catálogos de imagens fornecem muitas definições de configuração do servidor, assim como fontes, perfis ICC e macros de comandos.

Eles mapeiam ids de imagem e conteúdo estático usadas em solicitações para caminhos de arquivos reais, armazenam vários metadados de imagem, como mapas de imagem, e fornecem containers para modelos e conjuntos de imagens.

Os catálogos de imagens são acessados somente pelo [!DNL Platform Server], nunca pelo Servidor de imagens. Os arquivos de atributo de catálogo devem ter um sufixo .ini e ser colocados na pasta de catálogo de [!DNL Platform Server] ( `PS::CatalogFolder`). Pelo menos o catálogo de imagens padrão é necessário e deve ser preenchido com todos os atributos para o funcionamento correto do [!DNL Platform Server].
