---
title: Suporte a pontos de acesso e mapas de imagem
description: Suporte a pontos de acesso e mapas de imagem
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 8d5dbc2d2b5e228f8496fd71633bf1cb96218226
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Suporte a pontos de acesso e mapas de imagem{#hotspot-and-image-maps-support}

O visualizador é compatível com a renderização de ícones de pontos de acesso e regiões de mapa de imagem na parte superior da exibição principal. A aparência dos ícones e das regiões dos pontos de acesso é controlada por meio do CSS, conforme descrito na seção Personalizar pontos de acesso e mapas de imagem.

Consulte [Mapas de imagens e pontos de acesso](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Os pontos de acesso e regiões podem ativar um recurso de Visualização rápida na página da Web de hospedagem acionando um retorno de chamada do JavaScript ou redirecionar um usuário para uma página da Web externa.

## Pontos de acesso do Quickview {#section-cda48fc9730142d0bb3326bac7df3271}

Esses tipos de pontos de acesso ou mapas de imagem devem ser criados usando o tipo de ação &quot;Visualização rápida&quot; no Dynamic Media, do Adobe Experience Manager. Quando um usuário ativa um ponto de acesso ou mapa de imagem, o visualizador executa o retorno de chamada do JavaScript `quickViewActivate` e passa os dados do ponto de acesso ou mapa de imagem para ele. Espera-se que a página da Web de incorporação acompanhe esse retorno de chamada. Ao acionar a página, ele abre sua própria implementação do Quickview.

## Redirecionar para página da Web externa {#section-ef820c71251e4215800bb99c0c9ebe16}

Pontos de acesso ou mapas de imagem criados para o tipo de ação &quot;Quickview&quot; no Dynamic Media do Experience Manager redireciona o usuário para um URL externo. Dependendo das configurações feitas durante a criação, o URL é aberto em uma nova guia do navegador, na mesma janela ou na janela do navegador nomeada.
