---
description: Inverter camada. Vira a camada na horizontal, na vertical ou em ambas, depois de aplicar o recorte= e antes de girar= e estender=.
seo-description: Inverter camada. Vira a camada na horizontal, na vertical ou em ambas, depois de aplicar o recorte= e antes de girar= e estender=.
seo-title: flip
solution: Experience Manager
title: flip
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d28631f3-2198-4ba3-ab4b-578832db926e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# flip{#flip}

Inverter camada. Vira a camada na horizontal, na vertical ou em ambas, depois de aplicar o recorte= e antes de girar= e estender=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr  </span> </p> </td> 
  <td class="stentry"> <p>Inverter camada horizontalmente (esquerda-direita). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud  </span> </p> </td> 
  <td class="stentry"> <p>Virar camada verticalmente (para cima e para baixo). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud  </span> </p> </td> 
  <td class="stentry"> <p>Inverta horizontal e verticalmente. </p> </td> 
 </tr> 
</table>

Pode também ser aplicado a camadas de texto.

Alguns comandos, incluindo `extend=`, aplicam-se implicitamente à camada 0 em vez da camada composta quando `layer=comp` é selecionado. Nesses cenários, todos os comandos atribuídos automaticamente à camada 0 serão aplicados antes dos comandos que se aplicam a `layer=comp`. Portanto, quando `layer=comp`, `extend=` é aplicado antes de `flip=`.

>[!NOTE]
>
>A camada virada é posicionada com base na âncora da camada; valores flip= diferentes resultarão em posições de camada diferentes quando a âncora não estiver localizada no centro da camada.

## Propriedades {#section-294da2af7be746b5adfc35e29ee68217}

comando Camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-502044f81a89492198d5f12a738459ea}

Nenhum.

## Consulte também {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
