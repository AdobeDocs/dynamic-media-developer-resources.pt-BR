---
title: pos
description: Posição da camada.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# pos{#pos}

Posição da camada.

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Deslocamento de pixel da origem desta camada para a origem da camada 0 (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Deslocamento normalizado da origem desta camada para a origem da camada 0 (real, real). </p></td> 
 </tr> 
</table>

Se houver uma imagem, texto e camadas de cores sólidas, `pos=` especifica a posição de uma âncora de camada em relação à âncora de camada 0. Os valores de coordenadas `posN=` são normalizados em relação ao tamanho reto real da camada 0.

Se houver camadas de efeito, `pos=` desloca a camada de efeito em relação à camada pai.

Os valores positivos movem a camada para a direita/para baixo e os negativos para a esquerda/para cima. No `posN=0.5,0.5`, ele move a camada pela metade da largura e altura da camada 0 para baixo e para a direita.

## Propriedades {#section-51a60cdc52d040538fef378ace7c2e7d}

Atributo de camada. Ignorado se `layer=0` ou `layer=comp`.

## Padrão {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. Essa coordenada coloca a âncora da camada no mesmo local que a âncora da camada 0 se for uma imagem, texto ou camada de cor sólida. Posiciona uma camada de efeito diretamente sobre ou sob sua camada principal.

## Exemplo {#section-a89a02c22f6b4260bfcf7c842cd6069d}

Consulte o Exemplo A em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consulte também {#section-812d95575ba542808e8387d0a8650606}

[origem=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
