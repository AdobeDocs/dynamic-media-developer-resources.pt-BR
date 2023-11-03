---
description: Configurações gerais do servidor
solution: Experience Manager
title: Geral
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Geral{#general}

Configurações gerais do servidor

## TC::PsPort - Porta de escuta principal {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Especifica a porta de escuta principal do [!DNL Platform Server]. Essa porta também é usada para acessar a documentação e as páginas de exemplo do Servidor de imagens, da Renderização de imagens e dos Visualizadores do Dynamic Media (se instalados).

## IS::CacheServerUrl - Url Raiz do Serviço de Cache {#section-bcca227a1f91453b834db4ea050968e2}

Especifica o caminho raiz HTTP para permitir o acesso do Servidor de imagens ao serviço de cache. Deve ser definido como [!DNL http://localhost:TC::PsPort /is/cache/secondary], com o número da porta correspondente `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - TTL Padrão do Image Source Remoto {#section-e4c31228b459492cacd2f482d9575f71}

O TTL para imagens em cache obtidas por meio de HTTP de uma fonte remota usando o `src={…}` construir. Usado somente quando o servidor remoto não inclui um cabeçalho de Expiração na resposta HTTP. Valor inteiro em segundos.

## IS::RemoteUrlTimeout - Tempo Limite do Image Source Remoto {#section-437646c479cc4bea81dae42100a3c50a}

O tempo que o Servidor de imagens aguarda um servidor remoto entregar o arquivo de imagem solicitado por meio de HTTP antes de retornar um erro. Valor inteiro em segundos.

## PS::allowDefaultCatalogRequests - Ativar/Desativar solicitações do catálogo padrão {#section-484e442a115a49b4ac269d1718b351e1}

Defina como falso para não permitir solicitações que não incluem uma ID de catálogo válida no caminho. O padrão é `true`. Quando definido como `false`, um erro é retornado para solicitações sem uma id de catálogo.

>[!NOTE]
>
>`req=catalogprops` não está sujeito a esta configuração.

## PS::saveToFile.saveTimeout - Tempo limite de salvamento de arquivo {#section-d22afd8ad86144b28684ed95a59db40e}

Valor padrão de tempo limite para `req=saveToFile` quando `timeout=`não foi especificado. `msec`. Um erro será retornado se a operação de salvamento não for concluída dentro do tempo especificado.
