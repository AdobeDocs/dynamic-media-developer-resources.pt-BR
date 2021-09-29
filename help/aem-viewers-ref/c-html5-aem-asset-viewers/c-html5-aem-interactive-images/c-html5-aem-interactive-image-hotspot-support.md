---
title: Suporte para pontos de conexão
description: Suporte para pontos de conexão
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# Suporte para pontos de conexão{#hotspot-support}

O visualizador suporta a renderização de ícones de ponto de acesso na parte superior da exibição principal. A aparência dos ícones de ponto de acesso é controlada pelo CSS, conforme descrito na seção Pontos de acesso .

Consulte [Pontos de acesso](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Os pontos de acesso podem ativar um recurso do Quickview na página da Web de hospedagem, acionando um retorno de chamada do JavaScript ou redirecionar um usuário para uma página da Web externa.

## Pontos de conexão do Quickview {#section-cda48fc9730142d0bb3326bac7df3271}

Esses tipos de pontos de acesso devem ser criados usando o tipo de ação &quot;QuickView&quot; no Dynamic Media, dos Ativos da Adobe Experience Manager - sob demanda. Quando um usuário ativa esse ponto de acesso, o visualizador executa o retorno de chamada `quickViewActivate` do JavaScript e transmite os dados do ponto de acesso a ele. Espera-se que a página da Web de incorporação escute essa chamada de retorno. Quando aciona a página, ela abre sua própria implementação do Quickview.

## Redirecionar para página da Web externa {#section-ef820c71251e4215800bb99c0c9ebe16}

Os pontos de acesso criados para a ação do tipo &quot;Exibição rápida&quot; no Dynamic Media de Ativos do Experience Manager - sob demanda redirecionam o usuário para um URL externo. Dependendo das configurações feitas durante a criação, o URL é aberto em uma nova guia do navegador, na mesma janela ou na janela do navegador nomeado.
