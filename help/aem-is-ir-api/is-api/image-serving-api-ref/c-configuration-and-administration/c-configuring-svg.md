---
description: O componente SvgRender é um aplicativo Java independente.
solution: Experience Manager
title: Configuração do SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---

# Configuração do SVG{#configuring-svg}

O componente SvgRender é um aplicativo Java independente.

As configurações do SVG estão localizadas em [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] e [!DNL ServerSupervisorRegistry.xml].

Uma conexão de soquete é usada para comunicação entre o SvgRender e o Servidor de imagens. O número da porta é 27346. Se necessário, ele pode ser alterado configurando `SVGRender.port` em [!DNL svg.conf] e `<SVGTcpPort>` em [!DNL ImageServerRegistry.xml] para um novo valor.

## Consulte também {#section-c085b47d54d44059bdaa67fd5e226e91}

[Configurações do SVG](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
