---
title: Suporte ao mapa de imagem
description: O Visualizador de catálogo eletrônico oferece suporte à renderização de ícones de mapa de imagem acima da exibição principal.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7a2a58f9-852e-4205-96bc-08332507b6cd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# Suporte ao mapa de imagem{#image-map-support}

O Visualizador de catálogo eletrônico oferece suporte à renderização de ícones de mapa de imagem acima da exibição principal.

A aparência dos ícones de mapa é controlada pelo CSS, conforme descrito em [Efeito do mapa de imagem](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Os mapas de imagem executam uma das três ações a seguir: redirecionar para uma página da Web externa, ativação pop-up do painel Informações e hiperlinks internos.

## Redirecionar para uma página da Web externa {#section-32ebe3c3a7f74892a428c5d48801de4d}

O `href` O atributo do mapa de imagem tem uma URL para o recurso externo, especificado explicitamente ou incluído em uma das funções de template JavaScript suportadas: `loadProduct()`, `loadProductCW()`e `loadProductPW()`.

Este é um exemplo de um redirecionamento de URL simples:

`href=http://www.adobe.com`

Neste exemplo, o mesmo URL é envolvido com a variável `loadProduct()` função:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Ao adicionar o código JavaScript na `HREF` do mapa de imagem, o código é executado no computador do cliente. Portanto, verifique se o código JavaScript é seguro.

## Ativação do pop-up do painel Informações {#section-7aa036420af646d1ad8cdc388add0b57}

Para trabalhar com painéis de Informações, um mapa de imagem tem a variável `ROLLOVER_KEY` conjunto de atributos. Além disso, defina a variável `href` ao mesmo tempo, caso contrário, o processamento de URL externo interfere na ativação pop-up do painel Informações.

Por fim, verifique se a configuração do visualizador inclui os valores apropriados para `InfoPanelPopup.template` e, opcionalmente, `InfoPanelPopup.infoServerUrl` parâmetros.

>[!NOTE]
>
>Ao configurar o Pop-up do painel Informações, o código do HTML e o código JavaScript passados para o Painel Informações são executados no computador do cliente. Portanto, verifique se esse código HTML e o código JavaScript estão protegidos.

## Hiperlinks internos {#section-6afa4fb2fe564c429e0201f019a95849}

Selecionar um mapa de imagem executa uma troca de página interna no visualizador. Para usar esse recurso, uma `href` no mapa de imagem tem o seguinte formato especial:

` href=target: *`idx`*`

Onde `*`idx`*` é um índice baseado em zero do spread do catálogo.

Este é um exemplo de um `href` atributo para um mapa de imagem que aponta para a distribuição 3D no eCatalog:

`href=target:2`
