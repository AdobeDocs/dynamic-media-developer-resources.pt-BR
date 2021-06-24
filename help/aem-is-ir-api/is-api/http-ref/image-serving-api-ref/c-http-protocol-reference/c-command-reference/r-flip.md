---
description: Flip Layer. Vira a camada horizontalmente, verticalmente ou em ambas, após aplicar cortar= e antes de girar= e estender=.
solution: Experience Manager
title: virar
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# virar{#flip}

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
