---
description: Configurações gerais do servidor
solution: Experience Manager
title: Geral
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
TQID: 'https://experienceleague.adobe.com/hjww7EYpf4xNxpUFQ1fudMOqNtokgykthwhonn78ZFE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# Geral{#general}

Configurações gerais do servidor

## TC::PsPort - Porta de escuta principal {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Especifica a porta de escuta principal para [!DNL Platform Server]. Essa porta também é usada para acessar a documentação e as páginas de exemplo do Servidor de imagens, da Renderização de imagens e dos Visualizadores do Dynamic Media (se instalados).

## IS::CacheServerUrl - Url Raiz do Serviço de Cache {#section-bcca227a1f91453b834db4ea050968e2}

Especifica o caminho raiz HTTP para permitir o acesso do Servidor de imagens ao serviço de cache. Deve ser definido como [!DNL http://localhost:TC::PsPort /is/cache/secondary], com o número da porta correspondente a `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - TTL Padrão do Image Source Remoto {#section-e4c31228b459492cacd2f482d9575f71}

O TTL para imagens em cache obtidas por meio de HTTP de uma origem remota usando a construção `src={…}`. Usado somente quando o servidor remoto não inclui um cabeçalho de Expiração na resposta HTTP. Valor inteiro em segundos.

## IS::RemoteUrlTimeout - Tempo Limite do Image Source Remoto {#section-437646c479cc4bea81dae42100a3c50a}

O tempo que o Servidor de imagens aguarda um servidor remoto entregar o arquivo de imagem solicitado por meio de HTTP antes de retornar um erro. Valor inteiro em segundos.

## PS::allowDefaultCatalogRequests - Ativar/Desativar solicitações do catálogo padrão {#section-484e442a115a49b4ac269d1718b351e1}

Defina como falso para não permitir solicitações que não incluem uma ID de catálogo válida no caminho. O padrão é `true`. Quando definido como `false`, um erro é retornado para solicitações sem uma ID de catálogo.

>[!NOTE]
>
>`req=catalogprops` não está sujeito a esta configuração.

## PS::saveToFile.saveTimeout - Tempo limite de salvamento de arquivo {#section-d22afd8ad86144b28684ed95a59db40e}

Valor de tempo limite padrão para `req=saveToFile` quando `timeout=` não está especificado. `msec`. Um erro será retornado se a operação de salvamento não for concluída dentro do tempo especificado.
