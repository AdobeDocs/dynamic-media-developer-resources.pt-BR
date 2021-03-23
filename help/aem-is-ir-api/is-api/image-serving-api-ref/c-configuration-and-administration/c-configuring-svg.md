---
description: O componente SvgRender é um aplicativo Java independente.
seo-description: O componente SvgRender é um aplicativo Java independente.
seo-title: Configuração de SVG
solution: Experience Manager
title: Configuração de SVG
uuid: f6e131af-283e-4649-b349-123489c0838d
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Configurando o SVG{#configuring-svg}

O componente SvgRender é um aplicativo Java independente.

As configurações de SVG estão localizadas em [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] e [!DNL ServerSupervisorRegistry.xml].

Uma conexão de soquete é usada para se comunicar entre o SvgRender e o Servidor de imagem. O número da porta é 27346. Se necessário, ele pode ser alterado ao definir `SVGRender.port` em [!DNL svg.conf] e `<SVGTcpPort>` em [!DNL ImageServerRegistry.xml] para um novo valor.

## Consulte também {#section-c085b47d54d44059bdaa67fd5e226e91}

[Configurações de SVG](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
