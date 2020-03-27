---
description: Configurações gerais do servidor
seo-description: Configurações gerais do servidor
seo-title: Geral
solution: Experience Manager
title: Geral
topic: Scene7 Image Serving - Image Rendering API
uuid: d7ec3dba-64b8-431b-b446-84ab6139ba8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Geral{#general}

Configurações gerais do servidor

## TC::PsPort - Porta de escuta principal {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Especifica a porta de escuta principal para o Servidor de plataforma. Essa porta também é usada para acessar a documentação e páginas de exemplo para o Serviço de imagem, Renderização de imagem e Visualizadores Scene7 (se instalados).

## IS::CacheServerUrl - URL raiz do serviço de cache {#section-bcca227a1f91453b834db4ea050968e2}

Especifica o caminho raiz HTTP para permitir o acesso do Servidor de imagens ao serviço de cache. Deve ser definido como [!DNL http://localhost:TC::PsPort /is/cache/secondary], com o número da porta correspondente `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - TTL Predefinido da Origem de Imagem Remota {#section-e4c31228b459492cacd2f482d9575f71}

O TTL para imagens em cache obtidas via HTTP de uma fonte remota usando a `src={…}` construção. Usado somente quando o servidor remoto não inclui um cabeçalho de Expiração na resposta HTTP. Valor inteiro em segundos.

## IS::RemoteUrlTimeout - Tempo Limite da Origem de Imagem Remota {#section-437646c479cc4bea81dae42100a3c50a}

A hora em que o Servidor de imagens aguardará um servidor remoto entregar o arquivo de imagem solicitado via HTTP antes de retornar um erro. Valor inteiro em segundos.

## PS::allowDefaultCatalogRequests - Enable/Disable Default Catalog Requests {#section-484e442a115a49b4ac269d1718b351e1}

Defina como falso para não permitir solicitações que não incluam uma ID de catálogo válida no caminho. O padrão é `true`. Quando definido como `false`, um erro é retornado para solicitações sem uma ID de catálogo.

>[!NOTE] {class=&quot;- tópico/observação &quot;}
>
>`req=catalogprops` não está sujeito a essa configuração.

## PS::saveToFile.saveTimeout - Tempo limite de salvamento do arquivo {#section-d22afd8ad86144b28684ed95a59db40e}

Valor de tempo limite padrão para `req=saveToFile` quando não `timeout=`é especificado. `msec`. Um erro será retornado se a operação de salvamento não for concluída dentro do tempo especificado.
