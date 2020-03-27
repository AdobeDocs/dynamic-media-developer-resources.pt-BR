---
description: O componente SvgRender é um aplicativo Java independente.
seo-description: O componente SvgRender é um aplicativo Java independente.
seo-title: Configuração do SVG
solution: Experience Manager
title: Configuração do SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: f6e131af-283e-4649-b349-123489c0838d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Configuração do SVG{#configuring-svg}

O componente SvgRender é um aplicativo Java independente.

As configurações de SVG estão localizadas em [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml]e [!DNL ServerSupervisorRegistry.xml].

Uma conexão de soquete é usada para se comunicar entre SvgRender e o Servidor de imagens. O número da porta é 27346. Se necessário, pode ser alterado ao configurar `SVGRender.port` em [!DNL svg.conf] e `<SVGTcpPort>` em [!DNL ImageServerRegistry.xml] para um novo valor.

## Consulte também {#section-c085b47d54d44059bdaa67fd5e226e91}

[Configurações de SVG](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
