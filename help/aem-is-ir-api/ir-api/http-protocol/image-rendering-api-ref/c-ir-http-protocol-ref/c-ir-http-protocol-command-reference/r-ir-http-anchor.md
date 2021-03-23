---
description: Âncora da imagem (ponto de acesso). Especifica o ponto de ancoragem de textura (ponto de conexão) da textura repetível ou do material de decalque.
seo-description: Âncora da imagem (ponto de acesso). Especifica o ponto de ancoragem de textura (ponto de conexão) da textura repetível ou do material de decalque.
seo-title: âncora
solution: Experience Manager
title: âncora
uuid: 1e695882-f97a-4208-b595-2851b91bdbfe
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# âncora{#anchor}

Âncora da imagem (ponto de acesso). Especifica o ponto de ancoragem de textura (ponto de conexão) da textura repetível ou do material de decalque.

`anchor= *``*, *`xy`*`

`anchorN= *``*, *`xnyn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,  <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Deslocamento de pixels do canto superior esquerdo da imagem de origem (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>,  <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>Deslocamento normalizado a partir do centro da imagem de origem (real, real). </p></td> 
 </tr> 
</table>

Uma textura repetível é aplicada a um objeto de vinheta, de modo que o ponto de ancoragem da textura ( `anchor=`) esteja localizado no ponto de origem da textura do objeto.

Uma imagem decal é aplicada a um objeto de vinheta, de modo que o ponto de ancoragem decal esteja localizado no ponto de origem decal do objeto. A posição de decalque pode ser ajustada usando o comando `pos=`.

`anchorN=0,0` posiciona a âncora da imagem no centro da imagem de origem. `anchorN=-0.5,-0.5` ou  `anchor=0,0` está no canto superior esquerdo e  `anchorN=0.5,0.5` está no canto inferior direito da imagem de origem.

## Propriedades {#section-91f929d35cd745ab9e1eeecf45fcedae}

**Atributo** de material. Ignorado se `align=2`, ou se o material não for uma textura repetível, um papel de parede ou um decalque.

## Padrão {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, se o material for baseado em uma entrada de catálogo. Caso contrário, `anchor=0,0` (o canto superior esquerdo da imagem) para texturas e papéis de parede repetíveis e `anchorN=0,0` (o centro da imagem) para decalques.

## Consulte também {#section-b18bf0b035644ca5aedebbc64373718e}

[catálogo::Âncora](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) ,  [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
