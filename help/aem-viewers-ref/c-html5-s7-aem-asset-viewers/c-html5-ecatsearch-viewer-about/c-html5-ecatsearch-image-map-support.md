---
description: O Visualizador de pesquisa do eCatalog é compatível com a renderização dos ícones de mapa de imagem acima da exibição principal.
solution: Experience Manager
title: Suporte a mapa de imagem
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 58e7523f-1615-4da4-bb09-a995bf427bfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Suporte a mapa de imagem{#image-map-support}

O Visualizador de pesquisa do eCatalog é compatível com a renderização dos ícones de mapa de imagem acima da exibição principal.

A aparência dos ícones de mapa é controlada por meio do CSS, conforme descrito em [Efeito do mapa de imagem](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Os mapas de imagem executam uma das três ações a seguir: redirecionar para uma página externa da Web, ativação pop-up do painel Informações e hiperlinks internos.

## Redirecionar para uma página externa da Web {#section-32ebe3c3a7f74892a428c5d48801de4d}

A variável `href` O atributo do mapa de imagem tem um URL para o recurso externo, especificado explicitamente ou encapsulado em uma das funções de template JavaScript compatíveis: `loadProduct()`, `loadProductCW()`, e `loadProductPW()`.

Veja a seguir um exemplo de um simples redirecionamento de URL:

`href=http://www.adobe.com`

Neste exemplo, o mesmo URL é encapsulado com a variável `loadProduct()` função:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Observe que quando você adicionar o código JavaScript no `HREF` do seu mapa de imagem, o código é executado no computador do cliente. Portanto, verifique se o código JavaScript é seguro.

## Ativação do pop-up Painel de informações {#section-7aa036420af646d1ad8cdc388add0b57}

Para trabalhar com painéis de Informações, um mapa de imagem tem o `ROLLOVER_KEY` conjunto de atributos. Além disso, defina a variável `href` atributo ao mesmo tempo, caso contrário, o processamento do URL externo interfere na ativação pop-up do painel Informações.

Por fim, verifique se a configuração do visualizador inclui os valores apropriados para `InfoPanelPopup.template` e, opcionalmente, `InfoPanelPopup.infoServerUrl` parâmetros.

>[!NOTE]
>
>Observe que, ao configurar o Pop-up Painel de informações, o código do HTML e o código do JavaScript passados para o Painel de informações serão executados no computador do cliente. Portanto, verifique se esse código de HTML e JavaScript são seguros.

## Hiperlinks internos {#section-6afa4fb2fe564c429e0201f019a95849}

Clicar em um mapa de imagem executa uma troca de página interna dentro do visualizador. Para usar esse recurso, um `href` o atributo no mapa de imagem tem o seguinte formato especial:

` href=target: *`idx`*`

onde `*`idx`*` é um índice baseado em zero da distribuição do catálogo.

Veja a seguir um exemplo de `href` atributo de um mapa de imagem que aponta para a página espelhada 3D no eCatalog:

`href=target:2`
