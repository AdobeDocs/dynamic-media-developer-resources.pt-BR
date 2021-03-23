---
description: Suporte para pontos de conexão
solution: Experience Manager
title: Suporte para pontos de conexão
uuid: 62e0e55a-55a3-417d-ad51-ec77a7c16ac3
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imagens interativas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Suporte a ponto de acesso{#hotspot-support}

O visualizador suporta a renderização de ícones de ponto de acesso na parte superior da exibição principal. A aparência dos ícones de ponto de acesso é controlada pelo CSS, conforme descrito na seção Pontos de acesso .

Consulte [Pontos de acesso](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Os pontos de acesso podem ativar um recurso de Exibição rápida na página da Web de hospedagem, acionando um retorno de chamada do JavaScript ou redirecionando um usuário para uma página da Web externa.

## Pontos de acesso da Exibição rápida {#section-cda48fc9730142d0bb3326bac7df3271}

Esses tipos de pontos de acesso devem ser criados usando o tipo de ação &quot;Exibição rápida&quot; no Dynamic Media, do AEM Assets - sob demanda. Quando um usuário ativa esse ponto de acesso, o visualizador executa o retorno de chamada `quickViewActivate` do JavaScript e transmite os dados do ponto de acesso a ele. Espera-se que a página da Web de incorporação escute essa chamada de retorno. Quando aciona a página, ela abre sua própria implementação da Exibição rápida.

## Redirecionar para página da Web externa {#section-ef820c71251e4215800bb99c0c9ebe16}

Os pontos de acesso criados para a ação do tipo &quot;Exibição rápida&quot; no Dynamic Media do AEM Assets - por demanda redirecionam o usuário para um URL externo. Dependendo das configurações feitas durante a criação, o URL é aberto em uma nova guia do navegador, na mesma janela ou na janela do navegador nomeado.
