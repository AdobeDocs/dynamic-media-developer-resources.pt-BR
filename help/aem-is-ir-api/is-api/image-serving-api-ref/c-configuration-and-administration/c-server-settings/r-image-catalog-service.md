---
description: Use essas configurações de servidor para o serviço de catálogo de imagens.
seo-description: Use essas configurações de servidor para o serviço de catálogo de imagens.
seo-title: Serviço de catálogo de imagens
solution: Experience Manager
title: Serviço de catálogo de imagens
topic: Scene7 Image Serving - Image Rendering API
uuid: 601b1c30-7d51-448b-97b5-5ad9cb383975
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Serviço de catálogo de imagens{#image-catalog-service}

Use essas configurações de servidor para o serviço de catálogo de imagens.

## CS::Catalog.rootPath - Pasta do catálogo de imagens {#section-02d107f157384b18835f884f24fea3aa}

Localização da pasta do catálogo de imagens (onde todos os [!DNL catalog.ini] arquivos devem estar localizados). Pode ser um caminho de arquivo absoluto ou um caminho relativo ao *[!DNL install_folder]*. O servidor monitora continuamente essa pasta e carrega ou recarrega catálogos quando um novo arquivo de catálogo principal (com sufixo de [!DNL .ini] arquivo) é detectado ou quando a última hora modificada de um arquivo de catálogo principal existente foi alterada.

## CS::Catalog.cacheRoot - Pasta de cache de catálogo {#section-73e499c3a5974f1aa4251e70272ff503}

A pasta raiz do cache do sistema de catálogo. Pode ser definida como uma das pastas em `PS::cache.rootPaths`. A pasta deve ser criada manualmente antes que essa configuração seja alterada.

## CS::Catalog.modifyWaitTime - Atraso na análise do arquivo do catálogo {#section-7348065bcc124cb68ea947bf1b9b0845}

Tempo em ms que o serviço de catálogo aguarda depois que um [!DNL catalog.ini] arquivo é alterado até que carregue os arquivos de catálogo secundários. Esse atraso ajuda a garantir que todos os arquivos de catálogo secundário estejam atualizados antes que o serviço de catálogo tente carregá-los. Valor inteiro em mseg.

## CS::Catalog.refreshInterval - Frequência de verificação de arquivo do catálogo {#section-517fefc1d8784777a1026abec8630d58}

Frequência na qual o serviço de catálogo verificará se há alterações nos catálogos de imagens. Valor inteiro em mseg.
