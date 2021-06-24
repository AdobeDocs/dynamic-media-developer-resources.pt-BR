---
description: Configurações gerais do servidor
solution: Experience Manager
title: Geral
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Geral{#general}

Configurações gerais do servidor

## TC::PsPort - Porta de escuta Principal {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Especifica a porta de escuta principal do Servidor de Plataforma. Essa porta também é usada para acessar a documentação e as páginas de exemplo do Serviço de imagem, Renderização de imagem e os Visualizadores do Dynamic Media (se instalados).

## IS::CacheServerUrl - Url Raiz do Serviço de Cache {#section-bcca227a1f91453b834db4ea050968e2}

Especifica o caminho raiz HTTP para permitir o acesso do Servidor de Imagens ao serviço de cache. Deve ser definido como [!DNL http://localhost:TC::PsPort /is/cache/secondary], com o número da porta correspondente a `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - TTL Padrão do Image Source Remoto {#section-e4c31228b459492cacd2f482d9575f71}

O TTL para imagens em cache obtidas via HTTP de uma fonte remota usando a construção `src={…}`. Usado apenas quando o servidor remoto não inclui um cabeçalho Expiration na resposta HTTP. Valor inteiro em segundos.

## IS::RemoteUrlTimeout - Tempo limite remoto do Image Source {#section-437646c479cc4bea81dae42100a3c50a}

O tempo que o Servidor de Imagem aguardará para um servidor remoto entregar o arquivo de imagem solicitado via HTTP antes de retornar um erro. Valor inteiro em segundos.

## PS::allowDefaultCatalogRequests - Ativar/Desativar solicitações padrão do catálogo {#section-484e442a115a49b4ac269d1718b351e1}

Defina como falso para não permitir solicitações que não incluam uma ID de catálogo válida no caminho. O padrão é `true`. Quando definido como `false`, um erro é retornado para solicitações sem uma id de catálogo.

>[!NOTE]
>
>`req=catalogprops` não está sujeito a essa configuração.

## PS::saveToFile.saveTimeout - Tempo limite de gravação de arquivo {#section-d22afd8ad86144b28684ed95a59db40e}

Valor de tempo limite padrão para `req=saveToFile` quando `timeout=`não é especificado. `msec`. Um erro será retornado se a operação de salvamento não for concluída dentro do período especificado.
