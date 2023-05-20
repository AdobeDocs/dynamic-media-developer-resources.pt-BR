---
description: Contém configurações relacionadas ao gerenciamento de catálogos de imagens.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

Contém configurações relacionadas ao gerenciamento de catálogos de imagens.

Este arquivo é um arquivo de propriedades JAVA. deve ter-se o cuidado de seguir as convenções adequadas; caso contrário, a [!DNL Platform Server] pode falhar ao iniciar. Use uma barra invertida dupla &#39;\\&#39; ou uma barra invertida simples &#39;/&#39; em vez de uma barra invertida &#39;\&#39; nos caminhos de arquivo do Windows. A barra invertida é usada como um caractere de escape neste tipo de arquivo.

As alterações feitas nesse arquivo entrarão em vigor logo após serem salvas.

Somente as configurações listadas abaixo podem ser alteradas em [!DNL catalog-service.conf]. Se uma configuração específica estiver ausente, ela poderá ser adicionada em qualquer lugar no arquivo. Somente uma instância de cada configuração pode estar presente.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
