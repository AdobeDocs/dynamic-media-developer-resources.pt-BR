---
description: Esses comandos podem ser usados para definir efeitos de camada, como sombra projetada ou efeitos de brilho. As camadas de efeito ignoram todos os outros comandos.
seo-description: Esses comandos podem ser usados para definir efeitos de camada, como sombra projetada ou efeitos de brilho. As camadas de efeito ignoram todos os outros comandos.
seo-title: Comandos de efeito de camada
solution: Experience Manager
title: Comandos de efeito de camada
topic: Scene7 Image Serving - Image Rendering API
uuid: 5fef90d1-0507-497b-9187-869672996852
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Comandos de efeito de camada{#layer-effect-commands}

Esses comandos podem ser usados para definir efeitos de camada, como sombra projetada ou efeitos de brilho. As camadas de efeito ignoram todos os outros comandos.

<table id="simpletable_3094B9783772437FAACF9B382F7A32EE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172" type="reference" format="dita" scope="local"> blendMode</a> </p></td> 
  <td class="stentry"> <p>Especifica o modo de mesclagem de camada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md" type="reference" format="dita" scope="local"> cor</a> </p></td> 
  <td class="stentry"> <p>Especifica a cor e a opacidade do efeito principal. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135" type="reference" format="dita" scope="local"> efeito</a> </p></td> 
  <td class="stentry"> <p>Start o segmento de camada de efeito e especifica a ordem z. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464" type="reference" format="dita" scope="local"> maskUse</a> </p></td> 
  <td class="stentry"> <p>Especifica como usar a máscara de camada do pai (canal alfa). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-blur.md#reference-00638f29e59b49c99f6bba27daf24668" type="reference" format="dita" scope="local"> op_blur</a> </p></td> 
  <td class="stentry"> <p>Pena o efeito. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a" type="reference" format="dita" scope="local"> op_growth</a> </p></td> 
  <td class="stentry"> <p>Aumenta ou reduz o efeito da camada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-noise.md#reference-763c4a890fe24bb6bb5ae9dad4e2da94" type="reference" format="dita" scope="local"> op_noise</a> </p></td> 
  <td class="stentry"> <p>Adiciona ruído ao efeito. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5" type="reference" format="dita" scope="local"> opaco</a> </p></td> 
  <td class="stentry"> <p>Reduz a opacidade da camada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143" type="reference" format="dita" scope="local"> po</a> </p></td> 
  <td class="stentry"> <p>Posiciona a camada de efeito em relação à camada pai. </p></td> 
 </tr> 
</table>
