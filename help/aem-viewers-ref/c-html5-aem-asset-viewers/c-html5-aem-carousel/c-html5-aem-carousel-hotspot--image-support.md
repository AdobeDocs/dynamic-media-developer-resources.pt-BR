---
description: Suporte a mapas de imagem e pontos de conexão
solution: Experience Manager
title: Suporte a mapas de imagem e pontos de conexão
topic: Dynamic Media
uuid: 839b6a7f-4f6f-43ad-8eb8-254959c7fbac
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# Suporte a mapas de imagem e pontos de conexão{#hotspot-and-image-maps-support}

O visualizador suporta a renderização de ícones de ponto de acesso e regiões de mapa de imagem na parte superior da visualização principal. A aparência dos ícones de ponto de acesso e das regiões é controlada pelo CSS, conforme descrito na seção personalizar Pontos de acesso e mapas de imagem.

Consulte [Pontos de acesso e mapas de imagem](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Os pontos de conexão e as regiões podem ativar um recurso de Visualização rápida na página da Web de hospedagem acionando um retorno de chamada JavaScript ou redirecionar um usuário para uma página da Web externa.

## Pontos de conexão de Visualização rápida {#section-cda48fc9730142d0bb3326bac7df3271}

Esses tipos de hotspots ou mapas de imagem devem ser criados usando o tipo de ação &quot;Visualização rápida&quot; no Dynamic Media, de AEM. Quando um usuário ativa um ponto de acesso ou mapa de imagem, o visualizador executa o `quickViewActivate` retorno de chamada JavaScript e transmite os dados do ponto de acesso ou mapa de imagem para ele. Espera-se que a página da Web de incorporação escute esse retorno de chamada. Quando aciona a página, ela abre sua própria implementação de Visualização Rápida.

## Redirecionar para página da Web externa {#section-ef820c71251e4215800bb99c0c9ebe16}

Pontos de acesso ou mapas de imagem criados para o tipo de ação &quot;Visualização rápida&quot; no Dynamic Media de AEM redireciona o usuário para um URL externo. Dependendo das configurações feitas durante a criação, o URL será aberto em uma nova guia do navegador, na mesma janela ou na janela do navegador nomeado.
