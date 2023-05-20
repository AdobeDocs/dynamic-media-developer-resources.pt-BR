---
title: Notas de compatibilidade
description: Notas de compatibilidade para sistemas operacionais, navegadores e dispositivos móveis.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---

# Notas de compatibilidade{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Notas de compatibilidade para sistemas operacionais, navegadores e dispositivos móveis.

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibilidade com conjuntos de vídeos adaptáveis mais antigos. Recarregue os conjuntos de vídeos adaptados para permitir reprodução.

## Geral {#section-7b9a9fcba85148d1802b7b3016b48e02}

* O dimensionamento do lado do navegador faz com que a interface do usuário e as imagens fiquem turvas à medida que o usuário amplia a página. A formatação da interface do usuário também é exibida incorretamente, dependendo do zoom, e é transferida para a tela inteira.
* Devido à limitação de tamanho nos dispositivos móveis, o Visualizador de mídia mista usa o gesto de slide para trocar quadros em conjuntos de imagens incorporadas, em vez de tocar no componente de amostras incorporadas. O componente está lá como um indicador visual.
* Em navegadores Internet Explorer e alguns dispositivos de toque, o modo de tela cheia não ocupa toda a tela do dispositivo. Em vez disso, ele redimensiona o aplicativo para o tamanho da janela do navegador.
* O botão Fechar não funciona no iOS 8.0 e no iOS 8.1, mas funciona no iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Vazamento de memória observado com visualizadores de Zoom e eCatalog. A navegação repetida pelos quadros faz com que o navegador falhe.
* Tocar duas vezes em um visualizador faz com que a página inteira aplique zoom em vez de apenas no visualizador com o dimensionamento do lado do navegador ativado.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Dispositivo detectado como tablet no modo retrato com Tela cheia nas configurações do navegador.

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Tocar duas vezes em um visualizador faz com que a página inteira aplique zoom em vez de somente no visualizador, com o dimensionamento do lado do navegador ativado.

## Galaxy Nexus 10 e Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* O eCatalog mostra páginas espelhadas incorretas com orientações de retrato e paisagem.

## Dispositivos móveis HTC {#section-dc42c80414c842e488738fc157c55b01}

* A incapacidade de desativar o pinch-zoom nativo é um &quot;recurso&quot; do invólucro da interface do usuário HTC (HTC Sense). Esse recurso pode fazer com que uma página inteira use o zoom ao usar o gesto de &quot;apertar para aplicar zoom&quot; no visualizador. Em vez disso, use um gesto de toque duplo.
* Os ícones de mapa de imagem se sobrepõem se os mapas de imagem forem pequenos e estiverem próximos.

## Visualizador de vídeo HTML5 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` O modificador só é compatível com o software HLS e a reprodução de HDS do Flash. Não funciona quando a reprodução está usando o reprodutor nativo.
* Reprodução progressiva OGG e WebM não suportada.
* O dimensionamento do navegador faz com que o reprodutor de vídeo seja exibido em um tamanho incorreto (inclui configurações de Exibição do painel de controle do Windows®).
* As buscas de vídeo usando o streaming HLS no Safari são inconsistentes.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Não há suporte para o modo Quirks.
* Não há suporte para o modo de compatibilidade.
* Não há suporte para o Internet Explorer em dispositivos móveis.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Catálogos eletrônicos grandes fazem com que o navegador trave no iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 ou posterior: as configurações do plug-in da Internet impedem a reprodução de vídeo do Flash.
* As buscas de vídeo usando o streaming HLS no Safari são inconsistentes.
* Não é possível buscar o fim do vídeo no Safari 6 usando o streaming HLS.
