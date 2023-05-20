---
description: Os componentes do Servidor de imagens são gerenciados pelo Supervisor do servidor, que é um daemon Linux ou Serviço do Windows (S7Supervisor.exe, listado como "Servidor de imagens do Dynamic Media" no Painel de controle Serviços).
solution: Experience Manager
title: Supervisor de servidor
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# Supervisor de servidor{#server-supervisor}

Os componentes do Servidor de imagens são gerenciados pelo Supervisor do servidor, que é um daemon Linux ou Serviço do Windows (S7Supervisor.exe, listado como &quot;Servidor de imagens do Dynamic Media&quot; no Painel de controle Serviços).

Além de iniciar e parar outros componentes do Servidor de imagens, o Supervisor de servidores é responsável por garantir a integridade desses outros componentes. Se um componente falhar, ele será reiniciado automaticamente para minimizar interrupções do serviço.

## Início e interrupção {#section-061d28d74e034a30adc39ea3e2031cd0}

O Supervisor de Servidor é iniciado, interrompido e reiniciado com o script do utilitário Servidor de Imagens. Consulte a [Documentação de utilitários](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) para obter mais informações.

Iniciar e parar o Supervisor de Servidor inicia e interrompe automaticamente todos os outros componentes do Servidor de Imagens.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
