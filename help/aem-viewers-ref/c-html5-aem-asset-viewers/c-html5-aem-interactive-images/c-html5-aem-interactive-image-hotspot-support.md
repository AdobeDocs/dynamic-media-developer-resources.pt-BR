---
description: Suporte para pontos de conexão
solution: Experience Manager
title: Suporte para pontos de conexão
topic: Dynamic Media
uuid: 62e0e55a-55a3-417d-ad51-ec77a7c16ac3
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# Suporte a hotspots{#hotspot-support}

O visualizador suporta a renderização de ícones de ponto de acesso na parte superior da visualização principal. A aparência dos ícones de hotspot é controlada pelo CSS, conforme descrito na seção Hotspots.

Consulte [Pontos de conexão](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Os pontos de acesso podem ativar um recurso de Visualização rápida na página da Web de hospedagem, acionando um retorno de chamada JavaScript ou redirecionar um usuário para uma página da Web externa.

## Pontos de conexão de Visualização rápida {#section-cda48fc9730142d0bb3326bac7df3271}

Esses tipos de hotspots devem ser criados usando o tipo de ação &quot;Visualização rápida&quot; no Dynamic Media, do AEM Assets - sob demanda. Quando um usuário ativa tal ponto de acesso, o visualizador executa o `quickViewActivate` retorno de chamada JavaScript e transmite os dados do ponto de acesso para ele. Espera-se que a página da Web de incorporação escute esse retorno de chamada. Quando aciona a página, ela abre sua própria implementação de Visualização Rápida.

## Redirecionar para página da Web externa {#section-ef820c71251e4215800bb99c0c9ebe16}

Pontos de conexão criados para o tipo de ação &quot;Visualização rápida&quot; no Dynamic Media do AEM Assets - a pedido redireciona o usuário para um URL externo. Dependendo das configurações feitas durante a criação, o URL será aberto em uma nova guia do navegador, na mesma janela ou na janela do navegador nomeado.
