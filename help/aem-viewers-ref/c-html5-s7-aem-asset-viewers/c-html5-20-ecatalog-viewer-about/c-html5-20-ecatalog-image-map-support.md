---
description: O Visualizador de catálogo eletrônico oferece suporte à renderização de ícones de mapa de imagem acima da exibição principal.
solution: Experience Manager
title: Suporte ao mapa de imagem
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---


# Suporte ao mapa de imagem{#image-map-support}

O Visualizador de catálogo eletrônico oferece suporte à renderização de ícones de mapa de imagem acima da exibição principal.

A aparência dos ícones de mapa é controlada por meio do CSS, conforme descrito em [Image map Effect](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Os mapas de imagem executam uma das três ações a seguir: redirecionar para uma página da Web externa, ativação pop-up do painel Informações e hiperlinks internos.

## Redirecionar para uma página da Web externa {#section-32ebe3c3a7f74892a428c5d48801de4d}

O atributo `href` do mapa de imagem tem um URL para o recurso externo, especificado explicitamente ou envolvido em uma das funções de template JavaScript suportadas: `loadProduct()`, `loadProductCW()` e `loadProductPW()`.

Este é um exemplo de um redirecionamento de URL simples:

`href=http://www.adobe.com`

Neste exemplo, o mesmo URL é envolvido com a função `loadProduct()` :

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Observe que, ao adicionar o código JavaScript ao atributo `HREF` do mapa de imagem, ele é executado no computador do cliente. Portanto, verifique se o código JavaScript é seguro.

## Ativação do pop-up do painel Informações {#section-7aa036420af646d1ad8cdc388add0b57}

Para trabalhar com painéis de Informações, um mapa de imagem tem o conjunto de atributos `ROLLOVER_KEY`. Além disso, defina o atributo `href` ao mesmo tempo, caso contrário, o processamento de URL externo interfere na ativação pop-up do painel Informações.

Por fim, verifique se a configuração do visualizador inclui os valores apropriados para os parâmetros `InfoPanelPopup.template` e, opcionalmente, `InfoPanelPopup.infoServerUrl`.

>[!NOTE]
>
>Observe que, ao configurar o Pop-up do painel Informações, o código HTML e o código JavaScript passados para o Painel Informações são executados no computador do cliente. Portanto, verifique se esse código HTML e código JavaScript estão seguros.

## Hiperlinks internos {#section-6afa4fb2fe564c429e0201f019a95849}

Clicar em um mapa de imagem executa uma troca de página interna no visualizador. Para usar esse recurso, um atributo `href` no mapa de imagem tem o seguinte formato especial:

` href=target: *`idx`*`

onde `*`idx`*` é um índice baseado em zero do spread do catálogo.

A seguir, um exemplo de um atributo `href` para um mapa de imagem que aponta para a distribuição 3D no eCatalog:

`href=target:2`
