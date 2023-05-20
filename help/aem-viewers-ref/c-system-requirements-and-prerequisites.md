---
title: Requisitos de sistema para visualizadores Dynamic Media HTML5
description: Requisitos de sistema para visualizadores Dynamic Media HTML5.
solution: Experience Manager
contentOwner: Rick Brough
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: e4543358-92a6-4acc-a8a2-227e1daea722
source-git-commit: 7793e9befcf3050b9f4e12deeffa018d7c91aaf7
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Requisitos do sistema de visualizadores Dynamic Media HTML5{#system-requirements}

Requisitos de sistema para visualizadores Dynamic Media HTML5.

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Hardware e software do servidor {#section-05099146f1f0418988c196635110bee6}

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

* Adobe Dynamic Media Image Serving 6.7.1 ou posterior.
* Visualizadores HTML5 exigem bibliotecas do lado do servidor JavaScript do SDK 3.11.5 ou posterior.
* *Enviar para um amigo* os recursos sociais exigem o s7ondemand 5.0.9 ou posterior.
* Visualizador de eCatalog - [Pop-up do painel Informações](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-infopanelpopup.md) o suporte exige o info server 2.1.8 ou posterior.
* Os componentes do recurso de pesquisa exigem o s7search 2.3.0 ou posterior.

## Requisitos de sistema dos visualizadores {#section-cc72b1e209524d038b4d5b92b35e998e}

**Requisitos mínimos do navegador do cliente para visualizadores de componentes:**

* Compatível com as seguintes versões de sistema operacional ou posteriores:
   * Microsoft® Windows® 7
   * macOS X 10.12
* Compatível com as seguintes versões de navegador/plataforma ou posteriores:
   * Android™ OS 4.x
   * BlackBerry® 10 em navegadores nativos. Somente a reprodução de vídeo é suportada.
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS6
   * iPad 2 (somente navegadores Safari e Chrome)
   * iPhone 3GS
   * Safari 11
* Não há suporte para o Internet Explorer em dispositivos móveis.
* *VisualizadorPanorâmico* O é compatível com as seguintes versões de navegador/plataforma ou posteriores:
   * Android™ 4.4 (somente dispositivos de telefone)
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11
* *Video360Viewer* e *DimensionalViewer* O é compatível com as seguintes versões de navegador/plataforma ou posteriores:
   * Android™ 5 (somente dispositivos de telefone)
   * Chrome 82
   * Edge
   * Firefox 77
   * iOS 12
   * Safari 12
* *ZoomVerticalViewer* O é compatível com as seguintes versões de navegador/plataforma ou posteriores:
   * Android™ 4.x
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11

## Fim de suporte para TLS 1.0 e 1.1 {#tls}

<!-- CQDOC-19433 -->

A partir de 30 de setembro de 2022, o Adobe Dynamic Media Viewers encerrará o suporte para o seguinte:

* TLS (Transport Layer Security) 1.0 e 1.1
* As seguintes cifras fracas no TLS 1.2:
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
   * TLS_RSA_WITH_AES_256_GCM_SHA384
   * TLS_RSA_WITH_AES_256_CBC_SHA256
   * TLS_RSA_WITH_AES_256_CBC_SHA
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_AES_128_GCM_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_CAMELLIA_256_CBC_SHA
   * TLS_RSA_WITH_CAMELLIA_128_CBC_SHA
   * TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA
   * TLS_RSA_WITH_SDES_EDE_CBC_SHA

## Combinações de navegador da Web e sistema operacional não compatíveis com visualizadores do Dynamic Media {#browser-os-support}

<!-- CQDOC-19433 -->

Os visualizadores Adobe Dynamic Media não suportam as seguintes combinações de navegador da Web e sistema operacional:

* Internet Explorer 11 + Windows 7
* Internet Explorer 11 + Windows 8.1
* Internet Explorer 11 + Windows Phone 8.1
* Internet Explorer 11 + Atualização do Windows Phone 8.1
* Safari 6 + iOS 6.0.1
* Safari 7 + iOS 7.1
* Safari 7 + OS X 10.9 Mavericks
* Safari 8 + iOS 8.4
* Safari 8 + OS X 10.10 Yosemite

<!-- CQDOC-19433 -->

<!-- 
NOTE
Effective September 30, 2018, Adobe Dynamic Media Classic Viewers ended support of Transport Layer Security 1.0 (TLS 1.0). As such, Dynamic Media Classic no longer supports viewers on the following browsers/platforms that support TLS 1.0 (Adobe recommends using TLS 1.2 or later):

* Android™ 2.3.7
* Android™ 4.0.4
* Android™ 4.1.1
* Android™ 4.2.2
* Android™ 4.3
* Internet Explorer 7 on Window Vista®
* Internet Explorer 8 on Windows® XP
* Internet Explorer 8-10 on Windows® 7
* Internet Explorer 10 on Windows® Phone 8.0
* Safari 5.1.9 on Apple OS X 10.6.8
* Safari 6.0.4 on Apple OS X 10.8.4
* Java™ 6u45
* Java™ 7u25
* OpenSSL 0.9.8y
* Baidu January 2015

NOTE
FLASH VIEWERS END-OF-LIFE — Effective January 31, 2017, Adobe Dynamic Media Classic officially ended support for the Flash viewer platform. -->

