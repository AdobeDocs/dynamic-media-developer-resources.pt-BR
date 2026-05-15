---
title: pos
description: Posição da camada.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
TQID: 'https://experienceleague.adobe.com/9UMGN0TeM4mZ0IZI--dEA3KBYKOVhJxCJMZuPevlq8o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
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
