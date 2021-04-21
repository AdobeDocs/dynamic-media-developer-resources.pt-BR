---
description: O componente SvgRender é um aplicativo Java independente.
solution: Experience Manager
title: Configuração de SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---


# Configurando o SVG{#configuring-svg}

O componente SvgRender é um aplicativo Java independente.

As configurações de SVG estão localizadas em [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] e [!DNL ServerSupervisorRegistry.xml].

Uma conexão de soquete é usada para se comunicar entre o SvgRender e o Servidor de imagem. O número da porta é 27346. Se necessário, ele pode ser alterado ao definir `SVGRender.port` em [!DNL svg.conf] e `<SVGTcpPort>` em [!DNL ImageServerRegistry.xml] para um novo valor.

## Consulte também {#section-c085b47d54d44059bdaa67fd5e226e91}

[Configurações de SVG](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
