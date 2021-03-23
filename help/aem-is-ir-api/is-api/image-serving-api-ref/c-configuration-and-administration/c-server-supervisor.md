---
description: Os componentes do Image Serving são gerenciados pelo Server Supervisor, que é um daemon Linux ou Windows Service (S7Supervisor.exe, listado como "Dynamic Media Image Serving" no Painel de Controle de Serviços).
seo-description: Os componentes do Image Serving são gerenciados pelo Server Supervisor, que é um daemon Linux ou Windows Service (S7Supervisor.exe, listado como "Dynamic Media Image Serving" no Painel de Controle de Serviços).
seo-title: Supervisor do servidor
solution: Experience Manager
title: Supervisor do servidor
uuid: 6ac38d90-00ed-4d49-84f0-2e77e7a86d47
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---


# Supervisor do servidor{#server-supervisor}

Os componentes do Image Serving são gerenciados pelo Server Supervisor, que é um daemon Linux ou Windows Service (S7Supervisor.exe, listado como &quot;Dynamic Media Image Serving&quot; no Painel de Controle de Serviços).

Além de iniciar e parar outros componentes do Image Serving, o Supervisor de Servidor é responsável por garantir a integridade desses outros componentes. Em caso de falha de um componente, ele é reiniciado automaticamente para minimizar qualquer interrupção de serviço.

## Iniciar e parar {#section-061d28d74e034a30adc39ea3e2031cd0}

O Supervisor de Servidor é iniciado, interrompido e reiniciado com o script do utilitário Servidor de Imagens. Consulte a [Documentação de utilitários](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) para obter mais informações.

Iniciar e parar o Server Supervisor inicia e interrompe automaticamente todos os outros componentes do Image Serving.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
