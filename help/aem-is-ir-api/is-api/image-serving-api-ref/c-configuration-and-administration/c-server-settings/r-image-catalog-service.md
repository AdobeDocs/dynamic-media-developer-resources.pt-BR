---
description: Use essas configurações do servidor para o serviço de catálogo de imagens.
solution: Experience Manager
title: Serviço de catálogo de imagens
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---

# Serviço de catálogo de imagens{#image-catalog-service}

Use essas configurações do servidor para o serviço de catálogo de imagens.

## CS::catalog.rootPath - Pasta do catálogo de imagens {#section-02d107f157384b18835f884f24fea3aa}

Local da pasta do catálogo de imagens (onde todas as [!DNL catalog.ini] arquivos devem ser localizados). Pode ser um caminho de arquivo absoluto ou um caminho relativo ao *[!DNL install_folder]*. O servidor monitora continuamente essa pasta e carrega ou recarrega catálogos quando um novo arquivo de catálogo principal (com [!DNL .ini] file suffix) for detectado ou quando a hora da última modificação de um arquivo de catálogo principal existente for alterada.

## CS::catalog.cacheRoot - Pasta de cache do catálogo {#section-73e499c3a5974f1aa4251e70272ff503}

A pasta raiz do cache do sistema de catálogo. Pode ser definido como o mesmo que uma das pastas em `PS::cache.rootPaths`. A pasta deve ser criada manualmente antes que essa configuração seja alterada.

## CS::catalog.modifyWaitTime - Atraso de análise do arquivo de catálogo {#section-7348065bcc124cb68ea947bf1b9b0845}

Tempo em ms que o serviço de catálogo aguarda após um [!DNL catalog.ini] é alterado até carregar os arquivos do catálogo secundário. Esse atraso ajuda a garantir que todos os arquivos de catálogo secundários estejam atualizados antes que o serviço de catálogo tente carregá-los. Valor inteiro em ms.

## CS::catalog.refreshInterval - Frequência de verificação do arquivo de catálogo {#section-517fefc1d8784777a1026abec8630d58}

Frequência na qual o serviço de catálogo verificará alterações nos catálogos de imagens. Valor inteiro em ms.
