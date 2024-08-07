---
title: âncora
description: Âncora de imagem. Define o ponto de ancoragem da imagem, cor sólida ou retângulo da caixa delimitadora de texto, antes de aplicar transformações (crop=, scale=, rotate=, flip=). Também serve como centro de rotação para rotate=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# âncora{#anchor}

Âncora de imagem. Define o ponto de ancoragem da imagem, cor sólida ou retângulo da caixa delimitadora de texto, antes de aplicar transformações (crop=, scale=, rotate=, flip=). Também serve como centro de rotação para rotate=.

`anchor= *`coord`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span> </span> </p> </td> 
  <td class="stentry"> <p>deslocamento de pixel do canto superior esquerdo da imagem de origem (int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>deslocamento normalizado do centro da imagem de origem (real, real) </p></td> 
 </tr> 
</table>

O ponto de ancoragem é transformado com a imagem e se torna o ponto de origem da camada (a menos que `origin=` também seja especificado, nesse caso `anchor=` é usado somente como centro de rotação para `rotate=`).

`anchorN=0,0` coloca a âncora de imagem no centro da imagem de origem. `anchorN=-0.5,-0.5` ou `anchor=0,0` está no canto superior esquerdo e `anchorN=0.5,0.5` está no canto inferior direito da imagem de origem.

## Propriedades {#section-f08942bc6aae46a8b5d341faaff80640}

Atributo de imagem do Source. Aplica-se à camada atual ou à camada 0 se `layer=comp`.

## Padrão {#section-35d369fab1254f1a9b91684a6e169ad1}

Se `anchor=` não for especificado, catalog::Anchor será usado. Se `catalog::Anchor` não estiver definido, o centro do retângulo da imagem será usado (o mesmo que especificar `anchorN=0,0`).

Camadas de texto envolvendo `textPs=` e camadas envolvendo `clipPath=` podem ter diferentes âncoras padrão.

## Exemplo {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

Consulte o &quot;Exemplo C&quot; em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consulte também {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catálogo::Âncora](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [origem=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [girar=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Camadas de Texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
