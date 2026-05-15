---
title: Suporte a mapa de imagem
description: O eCatalog Viewer suporta a renderização de ícones de mapa de imagem acima da visualização principal.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7a2a58f9-852e-4205-96bc-08332507b6cd
TQID: 'https://experienceleague.adobe.com/x03fPe1hVRb3rIX7IaILspHHB0flCJ-iilhJs6TBL-k'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 304
ht-degree: 0%

---

# Suporte a mapa de imagem{#image-map-support}

O eCatalog Viewer suporta a renderização de ícones de mapa de imagem acima da visualização principal.

A aparência dos ícones do mapa é controlada por CSS, conforme descrito em [Efeito do mapa de imagem](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Os mapas de imagem executam uma das três ações a seguir: redirecionar para uma página externa da Web, ativação pop-up do painel Informações e hiperlinks internos.

## Redirecionar para uma página externa da Web {#section-32ebe3c3a7f74892a428c5d48801de4d}

O atributo `href` do mapa de imagem tem uma URL para o recurso externo, especificada explicitamente ou encapsulada em uma das funções de modelo de JavaScript com suporte: `loadProduct()`, `loadProductCW()` e `loadProductPW()`.

Veja a seguir um exemplo de um simples redirecionamento de URL:

`href=http://www.adobe.com`

Neste exemplo, a mesma URL é encapsulada com a função `loadProduct()`:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Ao adicionar o código JavaScript ao atributo `HREF` do mapa de imagem, ele é executado no computador do cliente. Portanto, verifique se o código JavaScript é seguro.

## Ativação do pop-up Painel de informações {#section-7aa036420af646d1ad8cdc388add0b57}

Para trabalhar com painéis de Informações, um mapa de imagem tem o atributo `ROLLOVER_KEY` definido. Além disso, defina o atributo `href` ao mesmo tempo. Caso contrário, o processamento da URL externa interfere na ativação pop-up do painel Informações.

Finalmente, verifique se a configuração do visualizador inclui os valores apropriados para `InfoPanelPopup.template` e, opcionalmente, `InfoPanelPopup.infoServerUrl` parâmetros.

>[!NOTE]
>
>Quando você configura o Pop-up Painel de Informações, o código do HTML e o código do JavaScript passados para o Painel de Informações são executados no computador do cliente. Portanto, verifique se esse código HTML e JavaScript são seguros.

## Hiperlinks internos {#section-6afa4fb2fe564c429e0201f019a95849}

A seleção de um mapa de imagem executa uma troca de página interna dentro do visualizador. Para usar esse recurso, um atributo `href` no mapa de imagem tem o seguinte formato especial:

` href=target: *`idx`*`

Onde `*`idx`*` é um índice baseado em zero da distribuição do catálogo.

Este é um exemplo de um atributo `href` para um mapa de imagem que aponta para a página espelhada 3D no eCatalog:

`href=target:2`
