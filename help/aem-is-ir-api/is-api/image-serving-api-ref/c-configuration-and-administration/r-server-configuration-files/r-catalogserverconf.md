---
description: Contém configurações relacionadas ao gerenciamento de catálogos de imagens.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# catalog-server.conf{#catalog-server-conf}

Contém configurações relacionadas ao gerenciamento de catálogos de imagens.

Esse arquivo é um arquivo de propriedades JAVA. Devem ser tomadas precauções para seguir as convenções adequadas; caso contrário, o servidor da plataforma poderá não ser iniciado. Use uma barra invertida dupla &#39;\&#39; ou uma barra invertida &#39;/&#39; em vez de uma barra invertida &#39;\&#39; nos caminhos de arquivo do Windows. A barra invertida é usada como um caractere de escape nesse tipo de arquivo.

As alterações nesse arquivo entrarão em vigor logo após o arquivo ser salvo.

Somente as configurações listadas abaixo podem ser alteradas em [!DNL catalog-service.conf]. Se uma configuração específica estiver ausente, ela poderá ser adicionada em qualquer lugar do arquivo. Apenas uma instância de cada configuração pode estar presente.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
