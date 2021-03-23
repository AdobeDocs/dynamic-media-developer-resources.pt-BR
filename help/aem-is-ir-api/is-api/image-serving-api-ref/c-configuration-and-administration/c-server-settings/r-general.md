---
description: Configurações gerais do servidor
seo-description: Configurações gerais do servidor
seo-title: Geral
solution: Experience Manager
title: Geral
uuid: d7ec3dba-64b8-431b-b446-84ab6139ba8a
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---


# Geral{#general}

Configurações gerais do servidor

## TC::PsPort - Porta de escuta principal {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Especifica a porta de escuta principal do Servidor de Plataforma. Essa porta também é usada para acessar a documentação e as páginas de exemplo do Serviço de imagem, Renderização de imagem e os Visualizadores do Dynamic Media (se instalados).

## IS::CacheServerUrl - URL raiz do serviço de cache {#section-bcca227a1f91453b834db4ea050968e2}

Especifica o caminho raiz HTTP para permitir o acesso do Servidor de Imagens ao serviço de cache. Deve ser definido como [!DNL http://localhost:TC::PsPort /is/cache/secondary], com o número da porta correspondente a `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - TTL Padrão da Fonte de Imagem Remota {#section-e4c31228b459492cacd2f482d9575f71}

O TTL para imagens em cache obtidas via HTTP de uma fonte remota usando a construção `src={…}`. Usado apenas quando o servidor remoto não inclui um cabeçalho Expiration na resposta HTTP. Valor inteiro em segundos.

## IS::RemoteUrlTimeout - Tempo Limite da Fonte de Imagem Remota {#section-437646c479cc4bea81dae42100a3c50a}

O tempo que o Servidor de Imagem aguardará para um servidor remoto entregar o arquivo de imagem solicitado via HTTP antes de retornar um erro. Valor inteiro em segundos.

## PS::allowDefaultCatalogRequests - Ativar/Desativar solicitações de catálogo padrão {#section-484e442a115a49b4ac269d1718b351e1}

Defina como falso para não permitir solicitações que não incluam uma ID de catálogo válida no caminho. O padrão é `true`. Quando definido como `false`, um erro é retornado para solicitações sem uma id de catálogo.

>[!NOTE]
>
>`req=catalogprops` não está sujeito a essa configuração.

## PS::saveToFile.saveTimeout - Tempo limite de gravação de arquivo {#section-d22afd8ad86144b28684ed95a59db40e}

Valor de tempo limite padrão para `req=saveToFile` quando `timeout=`não é especificado. `msec`. Um erro será retornado se a operação de salvamento não for concluída dentro do período especificado.
