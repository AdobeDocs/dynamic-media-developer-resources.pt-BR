---
description: Posição da camada.
solution: Experience Manager
title: pos
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# pos{#pos}

Posição da camada.

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cabo</span> </p> </td> 
  <td class="stentry"> <p>Deslocamento de pixels da origem dessa camada para a origem da camada 0 (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cordN</span> </p></td> 
  <td class="stentry"> <p>Deslocamento normalizado da origem dessa camada para a origem da camada 0 (real, real). </p></td> 
 </tr> 
</table>

No caso de imagens, texto e camadas de cores sólidas, `pos=` especifica a posição de uma âncora de camada em relação à âncora da camada 0. `posN=` os valores de coordenadas são normalizados em relação ao tamanho real de rett da camada 0.

No caso de camadas de efeito, `pos=` alterna a camada de efeito em relação à camada pai.

Valores positivos movem a camada para a direita/inferior, negativos para a esquerda/superior. `posN=0.5,0.5` move a camada em metade da largura e altura da camada 0 para baixo e para a direita.

## Propriedades {#section-51a60cdc52d040538fef378ace7c2e7d}

Atributo de camada. Ignorado se `layer=0` ou `layer=comp`.

## Padrão {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. Isso coloca a âncora da camada no mesmo local que a âncora da camada 0, se esta for uma imagem, texto ou camada de cor sólida. Posiciona uma camada de efeito diretamente sobre ou sob a camada pai.

## Exemplo {#section-a89a02c22f6b4260bfcf7c842cd6069d}

Consulte Exemplo A em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consulte também {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
