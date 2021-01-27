---
description: Notas de compatibilidade para sistemas operacionais, navegadores e dispositivos móveis.
seo-description: Notas de compatibilidade para sistemas operacionais, navegadores e dispositivos móveis.
seo-title: Notas de compatibilidade
solution: Experience Manager
title: Notas de compatibilidade
topic: Dynamic Media
uuid: cf732a03-bfaa-4838-862f-73343cefbd67
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---


# Notas de compatibilidade{#compatibility-notes}

<!-- Updated January 13,2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Notas de compatibilidade para sistemas operacionais, navegadores e dispositivos móveis.

## Blackberry {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibilidade com Conjuntos de vídeos adaptativos mais antigos. Talvez seja necessário recarregar os Conjuntos de vídeos adaptáveis para permitir a reprodução.

## Geral {#section-7b9a9fcba85148d1802b7b3016b48e02}

* O dimensionamento do lado do navegador pode fazer com que a interface do usuário e as imagens fiquem indefinidas à medida que o usuário aumenta o zoom na página. A formatação da interface também pode ser exibida incorretamente dependendo do zoom. Isso será levado para tela cheia.
* Devido à limitação de tamanho em dispositivos móveis, o Visualizador de mídia mista usa o gesto de slide para trocar quadros em conjuntos de imagens incorporados, em vez de tocar no componente de amostras incorporado. O componente está lá como um indicador visual.
* Nos navegadores Internet Explorer e em alguns dispositivos de toque, o modo de tela cheia não ocupa a tela inteira do dispositivo. Em vez disso, ele redimensiona o aplicativo para o tamanho da janela do navegador.
* O botão Fechar não funciona com o iOS 8.0 e o iOS 8.1, mas funciona com o iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Vazamento de memória observado com visualizadores de Zoom e eCatalog. A navegação repetida pelos quadros pode fazer com que o navegador falhe.
* Tocar no duplo em um visualizador pode fazer com que a página inteira aumente o zoom em vez de apenas o visualizador com a escala do lado do navegador ativada.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Dispositivo detectado como tablet no modo retrato com tela cheia marcada nas configurações do navegador.

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Tocar no duplo em um visualizador pode fazer com que a página inteira aumente o zoom em vez de apenas o visualizador, com a escala do lado do navegador ativada.

## Galaxy Nexus 10 e Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* O eCatalog mostra páginas espelhadas incorretas com orientações retrato e paisagem.

## Dispositivos móveis HTC {#section-dc42c80414c842e488738fc157c55b01}

* A incapacidade de desativar o zoom nativo de aproximação é um &quot;recurso&quot; do invólucro HTC UI (Sensor HTC). Esse recurso pode fazer com que uma página inteira aumente o zoom ao usar o gesto de &quot;aproximar o zoom&quot; no visualizador. Em vez disso, use um gesto de toque em duplo.
* Os ícones do mapa de imagem podem se sobrepor se os mapas de imagem forem pequenos e próximos.

## Visualizador de vídeo HTML5 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` o modificador só é suportado com o software HLS e a reprodução Flash HDS. Ela não funciona quando a reprodução está usando o player nativo.
* Reprodução progressiva de OGG e WebM não suportada.
* A escala do navegador pode fazer com que o player de vídeo seja exibido em um tamanho incorreto (incluindo as configurações de Exibição do painel de controle do SO do Windows).
* A busca de vídeo usando streaming HLS no Safari pode ser inconsistente.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* O modo Quirks não é suportado.
* O modo de compatibilidade não é suportado.
* O Internet Explorer em dispositivos móveis não é suportado.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Catálogos grandes podem fazer com que o navegador falhe no iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 ou posterior: As configurações de plug-in da Internet podem impedir a reprodução do vídeo do Flash.
* A busca de vídeo usando streaming HLS no Safari pode ser inconsistente.
* Não é possível buscar o fim do vídeo no Safari 6 usando o streaming HLS.
