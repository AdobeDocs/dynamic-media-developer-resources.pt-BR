---
description: O eCatalog Viewer suporta a renderização de ícones de mapa de imagem acima da visualização principal.
seo-description: O eCatalog Viewer suporta a renderização de ícones de mapa de imagem acima da visualização principal.
seo-title: Suporte ao mapa de imagens
solution: Experience Manager
title: Suporte ao mapa de imagens
topic: Dynamic media
uuid: 69aeda21-909d-45da-bcf5-73ade8c5adda
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# Suporte ao mapa de imagens{#image-map-support}

O eCatalog Viewer suporta a renderização de ícones de mapa de imagem acima da visualização principal.

A aparência dos ícones de mapa é controlada pelo CSS, conforme descrito em [Efeito do mapa de imagem](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Os mapas de imagem executam uma das três ações a seguir: redirecionar para uma página da Web externa, ativação pop-up do painel Informações e hiperlinks internos.

## Redirecionar para uma página da Web externa {#section-32ebe3c3a7f74892a428c5d48801de4d}

O atributo `href` do mapa de imagem tem um URL para o recurso externo, especificado explicitamente ou vinculado a uma das funções de modelo JavaScript suportadas: `loadProduct()`, `loadProductCW()` e `loadProductPW()`.

A seguir está um exemplo de um redirecionamento de URL simples:

`href=http://www.adobe.com`

Neste exemplo, o mesmo URL é encapsulado com a função `loadProduct()`:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Lembre-se de que quando você adiciona o código JavaScript ao atributo `HREF` do mapa de imagem, o código é executado no computador do cliente. Portanto, verifique se o código JavaScript está protegido.

## Ativação pop-up do painel Informações {#section-7aa036420af646d1ad8cdc388add0b57}

Para trabalhar com os painéis Informações, um mapa de imagem tem o conjunto de atributos `ROLLOVER_KEY`. Além disso, defina o atributo `href` ao mesmo tempo; caso contrário, o processamento de URL externo interfere na ativação pop-up do painel Informações.

Finalmente, certifique-se de que a configuração do visualizador inclui os valores apropriados para os parâmetros `InfoPanelPopup.template` e, opcionalmente, `InfoPanelPopup.infoServerUrl`.

>[!NOTE]
>
>Ao configurar o Pop-up do painel Informações, o código HTML e o código JavaScript passados para o Painel Informações são executados no computador do cliente. Portanto, verifique se o código HTML e o código JavaScript estão protegidos.

## Hiperlinks internos {#section-6afa4fb2fe564c429e0201f019a95849}

Clicar em um mapa de imagem executa uma troca de página interna no visualizador. Para usar esse recurso, um atributo `href` no mapa de imagem tem o seguinte formato especial:

` href=target: *`idx`*`

em que `*`idx`*` é um índice com base em zero da propagação do catálogo.

A seguir está um exemplo de um atributo `href` para um mapa de imagem que aponta para a distribuição 3D no eCatalog:

`href=target:2`
