---
description: Use essas configurações de servidor para caches de servidor.
solution: Experience Manager
title: Caches de servidores
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# Caches do servidor{#server-caches}

Use essas configurações de servidor para caches de servidor.

## PS::cache.rootPaths - Pastas de Dados de Cache {#section-f0aa808304d74ecdb0c3644f11906c53}

As pastas raiz do cache de disco do Servidor de plataforma. Um ou mais caminhos de arquivo absolutos ou caminhos relativos a *[!DNL install_folder]*, separados por ponto e vírgula (;). Os dados para o cache de resposta HTTP serão distribuídos uniformemente em todas as pastas especificadas. Os caches para os caches auxiliares (catálogos de imagens compilados e dados de imagens estrangeiras) estarão localizados na pasta de cache principal (a primeira pasta na lista).

## PS::cache.maxSize - Response Data Cache Size {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

O tamanho máximo do cache de resposta HTTP em bytes. Esta definição limita a quantidade de dados reais a armazenar em cache; não considera a sobrecarga do sistema de arquivos. (Consulte [Cache de Dados de Resposta](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca).) Se várias pastas de dados de cache forem especificadas, os dados do cache serão distribuídos uniformemente em todas as pastas. O valor de `cache.maxSize` em [!DNL PlatformServer.conf] está em bytes.

## PS::cache.maxEntries - Máximo de Entradas do Cache de Dados de Resposta {#section-5603e327e90542a5b50aeeb27b080410}

O número de entradas alocadas para o índice de cache de resposta HTTP na memória.

>[!NOTE]
>
>No Linux, verifique se os i-nós suficientes estão alocados para a partição de cache para evitar a execução de i-nós.

## IS::TempDirectory - Pasta de Arquivos Temporários do Servidor de Imagens {#section-42ea1e7a68c444878f7245c5bbcb1672}

Ocasionalmente, o Servidor de Imagens precisa salvar dados intermediários em disco. O caminho pode ser absoluto ou relativo a *[!DNL install_folder]*.

>[!NOTE]
>
>A nova pasta deve ser criada antes de alterar essa configuração. Verifique se as permissões de acesso estão definidas para que o Servidor de imagem tenha controle total da pasta.

## SV::temp - Pasta de Arquivos Temporários do Supervisor de Servidor {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

Ocasionalmente, o Server Supervisor precisa salvar dados intermediários no disco. O caminho pode ser absoluto ou relativo a *[!DNL install_folder]*. O padrão é [!DNL *[!DNL install_folder]*/temp].

>[!NOTE]
>
>A nova pasta deve ser criada antes de alterar essa configuração. Verifique se as permissões de acesso estão definidas para que o Server Supervisor tenha controle total da pasta.

