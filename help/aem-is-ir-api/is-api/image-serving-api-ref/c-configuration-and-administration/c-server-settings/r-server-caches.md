---
description: Use essas configurações do servidor para caches do servidor.
seo-description: Use essas configurações do servidor para caches do servidor.
seo-title: Caches do servidor
solution: Experience Manager
title: Caches do servidor
topic: Scene7 Image Serving - Image Rendering API
uuid: 73745363-2011-453f-b7a0-96de4b44186d
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# Caches do servidor{#server-caches}

Use essas configurações do servidor para caches do servidor.

## PS::cache.rootPaths - Pastas de dados de cache {#section-f0aa808304d74ecdb0c3644f11906c53}

As pastas raiz do cache de disco do Servidor de plataforma. Um ou mais caminhos de arquivo absolutos ou caminhos relativos a *[!DNL install_folder]*, separados por ponto-e-vírgula (;). Os dados do cache de resposta HTTP serão distribuídos uniformemente em todas as pastas especificadas. Os caches dos caches auxiliares (catálogos de imagens compilados e dados de imagens estrangeiras) estarão localizados na pasta de cache principal (a primeira pasta na lista).

## PS::cache.maxSize - Tamanho do Cache de Dados de Resposta {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

O tamanho máximo do cache de resposta HTTP em bytes. Esta definição limita a quantidade de dados reais a armazenar em cache; não considera a sobrecarga do sistema de arquivos. (Consulte [Cache de Dados de Resposta](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca).) Se várias pastas de dados de cache forem especificadas, os dados de cache serão distribuídos uniformemente em todas as pastas. O valor de `cache.maxSize` em [!DNL PlatformServer.conf] está em bytes.

## PS::cache.maxEntries - Máximo de Entradas do Cache de Dados de Resposta {#section-5603e327e90542a5b50aeeb27b080410}

O número de entradas alocadas para o índice de cache de resposta HTTP na memória.

>[!NOTE]
>
>No Linux, certifique-se de que sejam alocados i-nodes suficientes para a partição do cache, a fim de evitar a execução de i-nodes.

## IS::TempDirectory - Pasta de Arquivos Temporários do Servidor de Imagens {#section-42ea1e7a68c444878f7245c5bbcb1672}

Ocasionalmente, o Servidor de imagens precisa salvar dados intermediários em disco. O caminho pode ser absoluto ou relativo a *[!DNL install_folder]*.

>[!NOTE]
>
>A nova pasta deve ser criada antes de alterar essa configuração. Verifique se as permissões de acesso estão definidas para que o Servidor de imagens tenha controle total da pasta.

## SV::temp - Pasta de Arquivos Temporários do Supervisor de Servidor {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

Ocasionalmente, o Supervisor de Servidor precisa salvar dados intermediários no disco. O caminho pode ser absoluto ou relativo a *[!DNL install_folder]*. O padrão é [!DNL *[!DNL install_folder]*/temp].

>[!NOTE]
>
>A nova pasta deve ser criada antes de alterar essa configuração. Verifique se as permissões de acesso estão definidas para que o Supervisor de Servidor tenha controle total da pasta.

