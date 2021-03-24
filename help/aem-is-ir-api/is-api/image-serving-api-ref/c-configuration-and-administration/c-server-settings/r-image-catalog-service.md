---
description: Use essas configurações do servidor para o serviço de catálogo de imagens.
solution: Experience Manager
title: Serviço de catálogo de imagens
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Serviço de catálogo de imagens{#image-catalog-service}

Use essas configurações do servidor para o serviço de catálogo de imagens.

## CS::catalog.rootPath - Pasta do catálogo de imagens {#section-02d107f157384b18835f884f24fea3aa}

Localização da pasta do catálogo de imagens (onde todos os arquivos [!DNL catalog.ini] devem estar localizados). Pode ser um caminho de arquivo absoluto ou um caminho relativo a *[!DNL install_folder]*. O servidor monitora continuamente essa pasta e carrega ou recarrega catálogos quando um novo arquivo de catálogo principal (com [!DNL .ini] sufixo de arquivo) é detectado ou quando a hora da última modificação de um arquivo de catálogo principal existente foi alterada.

## CS::catalog.cacheRoot - Pasta de Cache de Catálogo {#section-73e499c3a5974f1aa4251e70272ff503}

A pasta raiz do cache do sistema de catálogo. Pode ser definido como o mesmo de uma das pastas em `PS::cache.rootPaths`. A pasta deve ser criada manualmente antes que essa configuração seja alterada.

## CS::catalog.modificationWaitTime - Atraso de análise do arquivo de catálogo {#section-7348065bcc124cb68ea947bf1b9b0845}

Tempo em ms, o serviço de catálogo aguarda depois que um arquivo [!DNL catalog.ini] é alterado até que carregue os arquivos de catálogo secundário. Esse atraso ajuda a garantir que todos os arquivos de catálogo secundário estejam atualizados antes que o serviço de catálogo tente carregá-los. Valor inteiro em ms.

## CS::catalog.refreshInterval - Frequência de verificação de arquivo do catálogo {#section-517fefc1d8784777a1026abec8630d58}

Frequência na qual o serviço de catálogo verificará se ocorreram alterações nos catálogos de imagens. Valor inteiro em ms.
