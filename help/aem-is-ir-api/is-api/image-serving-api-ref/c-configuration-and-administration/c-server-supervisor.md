---
description: Os componentes do Servidor de imagens são gerenciados pelo Supervisor de Servidor, que é um daemon Linux ou Serviço Windows (S7Supervisor.exe, listado como "Scene7 Image Serving" no Painel de controle do Campaign Serviços).
seo-description: Os componentes do Servidor de imagens são gerenciados pelo Supervisor de Servidor, que é um daemon Linux ou Serviço Windows (S7Supervisor.exe, listado como "Scene7 Image Serving" no Painel de controle do Campaign Serviços).
seo-title: Supervisor do servidor
solution: Experience Manager
title: Supervisor do servidor
topic: Scene7 Image Serving - Image Rendering API
uuid: 6ac38d90-00ed-4d49-84f0-2e77e7a86d47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Supervisor do servidor{#server-supervisor}

Os componentes do Servidor de imagens são gerenciados pelo Supervisor de Servidor, que é um daemon Linux ou Serviço Windows (S7Supervisor.exe, listado como &quot;Scene7 Image Serving&quot; no Painel de controle do Campaign Serviços).

Além de iniciar e parar outros componentes do Servidor de imagens, o Supervisor de Servidor é responsável por garantir a integridade desses outros componentes. Se um componente falhar, ele será reiniciado automaticamente para minimizar quaisquer interrupções de serviço.

## Iniciar e parar {#section-061d28d74e034a30adc39ea3e2031cd0}

O Supervisor de Servidor é iniciado, parado e reiniciado com o script do utilitário Servidor de Imagens. Consulte a documentação [Utilities](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) para obter mais informações.

Iniciar e parar o Supervisor de Servidor automaticamente start e interrompe todos os outros componentes do Servidor de imagens.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
