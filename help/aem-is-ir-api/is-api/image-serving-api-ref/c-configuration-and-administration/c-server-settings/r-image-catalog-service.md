---
description: Use essas configurações de servidor para o serviço de catálogo de imagens.
seo-description: Use essas configurações de servidor para o serviço de catálogo de imagens.
seo-title: Serviço de catálogo de imagens
solution: Experience Manager
title: Serviço de catálogo de imagens
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 601b1c30-7d51-448b-97b5-5ad9cb383975
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# Serviço de catálogo de imagens{#image-catalog-service}

Use essas configurações de servidor para o serviço de catálogo de imagens.

## CS::Catalog.rootPath - Pasta do catálogo de imagens {#section-02d107f157384b18835f884f24fea3aa}

Localização da pasta do catálogo de imagens (onde todos os arquivos [!DNL catalog.ini] devem estar localizados). Pode ser um caminho de arquivo absoluto ou um caminho relativo a *[!DNL install_folder]*. O servidor monitora continuamente essa pasta e carrega ou recarrega catálogos quando um novo arquivo de catálogo principal (com [!DNL .ini] sufixo de arquivo) é detectado ou quando a última hora modificada de um arquivo de catálogo principal existente é alterada.

## CS::Catalog.cacheRoot - Pasta de Cache de Catálogo {#section-73e499c3a5974f1aa4251e70272ff503}

A pasta raiz do cache do sistema de catálogo. Pode ser definida como uma das pastas em `PS::cache.rootPaths`. A pasta deve ser criada manualmente antes que essa configuração seja alterada.

## CS::Catalog.modifyWaitTime - Atraso de Análise do Arquivo de Catálogo {#section-7348065bcc124cb68ea947bf1b9b0845}

Tempo em ms, o serviço de catálogo aguarda após um arquivo [!DNL catalog.ini] ser alterado até que ele carregue os arquivos de catálogo secundários. Esse atraso ajuda a garantir que todos os arquivos de catálogo secundário estejam atualizados antes que o serviço de catálogo tente carregá-los. Valor inteiro em mseg.

## CS::Catalog.refreshInterval - Frequência de verificação de arquivo do catálogo {#section-517fefc1d8784777a1026abec8630d58}

Frequência na qual o serviço de catálogo verificará se há alterações nos catálogos de imagens. Valor inteiro em mseg.
