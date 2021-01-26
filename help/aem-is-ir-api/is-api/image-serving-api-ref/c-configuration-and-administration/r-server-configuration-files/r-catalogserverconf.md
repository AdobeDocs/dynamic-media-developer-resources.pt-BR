---
description: Contém configurações relacionadas ao gerenciamento de catálogos de imagens.
seo-description: Contém configurações relacionadas ao gerenciamento de catálogos de imagens.
seo-title: catalog-server.conf
solution: Experience Manager
title: catalog-server.conf
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 797a43d2-18f5-4735-8b19-da231952b1a2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# catalog-server.conf{#catalog-server-conf}

Contém configurações relacionadas ao gerenciamento de catálogos de imagens.

Este arquivo é um arquivo de propriedades JAVA. Devem ser tomadas precauções para seguir as convenções adequadas; caso contrário, o Servidor da plataforma poderá falhar no start. Use uma barra invertida de duplo &#39;\\&#39; ou uma barra invertida &#39;/&#39; em vez de uma barra invertida &#39;\&#39; nos caminhos de arquivos do Windows. A barra invertida é usada como um caractere de escape nesse tipo de arquivo.

As alterações neste arquivo entrarão em vigor logo após o arquivo ser salvo.

Somente as configurações listadas abaixo podem ser alteradas em [!DNL catalog-service.conf]. Se uma configuração específica estiver ausente, ela poderá ser adicionada em qualquer lugar do arquivo. Apenas uma instância de cada configuração pode estar presente.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
