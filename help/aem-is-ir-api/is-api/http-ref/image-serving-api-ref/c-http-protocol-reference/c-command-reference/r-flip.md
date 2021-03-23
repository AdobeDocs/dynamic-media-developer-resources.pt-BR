---
description: Flip Layer. Vira a camada horizontalmente, verticalmente ou em ambas, após aplicar cortar= e antes de girar= e estender=.
seo-description: Flip Layer. Vira a camada horizontalmente, verticalmente ou em ambas, após aplicar cortar= e antes de girar= e estender=.
seo-title: virar
solution: Experience Manager
title: virar
uuid: d28631f3-2198-4ba3-ab4b-578832db926e
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# flip{#flip}

Flip Layer. Vira a camada horizontalmente, verticalmente ou em ambas, após aplicar cortar= e antes de girar= e estender=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr  </span> </p> </td> 
  <td class="stentry"> <p>Virar a camada horizontalmente (à esquerda e à direita). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud  </span> </p> </td> 
  <td class="stentry"> <p>Virar camada verticalmente (para cima). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud  </span> </p> </td> 
  <td class="stentry"> <p>Inverter horizontalmente e verticalmente. </p> </td> 
 </tr> 
</table>

Pode também ser aplicado às camadas de texto.

Alguns comandos, incluindo `extend=`, aplicam-se implicitamente à camada 0 em vez da camada composta quando `layer=comp` é selecionado. Nesses cenários, todos os comandos que são atribuídos automaticamente à camada 0 serão aplicados antes dos comandos que se aplicam a `layer=comp`. Assim, quando `layer=comp`, `extend=` é aplicado antes de `flip=`.

>[!NOTE]
>
>A camada virada é posicionada com base na âncora da camada; valores flip= diferentes resultarão em posições de camada diferentes quando a âncora não estiver localizada no centro da camada.

## Propriedades {#section-294da2af7be746b5adfc35e29ee68217}

comando Camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. Ignorado por camadas de efeito.

## Padrão {#section-502044f81a89492198d5f12a738459ea}

Nenhum.

## Consulte também {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ,  [âncora=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
