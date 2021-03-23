---
description: Origem da camada.
seo-description: Origem da camada.
seo-title: origem
solution: Experience Manager
title: origem
uuid: a36fc0b6-7744-4c1c-b9f8-4aa31a886bff
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# origem{#origin}

Origem da camada.

`origin= *`cabo`*`

`originN= *`cordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cabo</span> </p></td> 
  <td class="stentry"> <p>Deslocamento de pixels do canto superior esquerdo da camada rect (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cordN</span> </p></td> 
  <td class="stentry"> <p>Deslocamento normalizado a partir do centro do retângulo da camada (real, real). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>O rett de camada sempre inclui qualquer modificação por `extend=`.

Define o ponto de alinhamento do retângulo da camada, que é usado para posicionar o retângulo da camada em relação à camada 0 via `pos=`. `originN=0,0` posiciona a origem da camada no centro do retângulo da camada. `originN=-0.5,-0.5` e  `origin=0,0` é o canto superior esquerdo, e  `originN=0.5,0.5` é o canto inferior direito do retângulo da camada.

## Propriedades {#section-60f639e36ada43d1abc6bfc100afc925}

Atributo de camada. Aplica-se à camada atual ou à camada 0, se `layer=comp`. Não afetado pelas transformações de camada ( `crop=`, `scale=`, `rotate=`, `flip=`) aplicadas à origem da camada. Substitui `anchor=`. Ignorado por camadas de efeito.

## Padrão {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

Se `origin=` não for especificado, a origem da camada será determinada pela aplicação das transformações de camada à âncora da imagem. Se a âncora da imagem não for conhecida, o centro do retângulo da camada ( `originN=0,0`) será usado.

## Exemplo {#section-13e38d6e17be4e6cbc6b27fbde63b291}

Consulte Exemplo A em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consulte também {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[âncora=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [estender=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
