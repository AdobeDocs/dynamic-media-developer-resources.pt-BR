---
title: Suporte a mapas de imagem e pontos de conexão
description: Suporte a mapas de imagem e pontos de conexão
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Suporte a mapas de imagem e pontos de conexão{#hotspot-and-image-maps-support}

O visualizador suporta a renderização de ícones de ponto de acesso e regiões de mapa de imagem na parte superior da exibição principal. A aparência de ícones de pontos de acesso e regiões é controlada pelo CSS, conforme descrito na seção personalizar pontos de acesso e mapas de imagem .

Consulte [Pontos de acesso e mapas de imagem](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Os pontos de conexão e as regiões podem ativar um recurso do Quickview na página da Web de hospedagem, acionando um retorno de chamada do JavaScript ou redirecionando um usuário para uma página da Web externa.

## Pontos de conexão do Quickview {#section-cda48fc9730142d0bb3326bac7df3271}

Esses tipos de pontos de acesso ou mapas de imagem devem ser criados usando o tipo de ação &quot;Quickview&quot; no Dynamic Media, do Adobe Experience Manager. Quando um usuário ativa um ponto de acesso ou mapa de imagem, o visualizador executa o retorno de chamada JavaScript `quickViewActivate` e transmite os dados do ponto de acesso ou mapa de imagem para ele. Espera-se que a página da Web de incorporação escute essa chamada de retorno. Quando aciona a página, ela abre sua própria implementação do Quickview.

## Redirecionar para página da Web externa {#section-ef820c71251e4215800bb99c0c9ebe16}

Pontos de acesso ou mapas de imagem criados para o tipo de ação &quot;Quickview&quot; no Dynamic Media do Experience Manager redireciona o usuário para uma URL externa. Dependendo das configurações feitas durante a criação, o URL é aberto em uma nova guia do navegador, na mesma janela ou na janela do navegador nomeado.
