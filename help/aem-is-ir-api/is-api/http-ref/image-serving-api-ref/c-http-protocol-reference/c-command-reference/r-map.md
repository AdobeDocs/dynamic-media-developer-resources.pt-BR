---
title: mapa
description: Dados do mapa de imagem. Fornece dados de mapa de imagem para esta camada. Substitui todos os dados do Mapa de catálogo para essa camada.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# mapa{#map}

Dados do mapa de imagem. Fornece dados de mapa de imagem para esta camada. Substitui todos os dados de catalog::Map dessa camada.

`map=[ *`string`*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Dados do mapa de imagem para esta camada em coordenadas de camada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>Dados do mapa de imagem para esta camada nas coordenadas da imagem de origem. </p></td> 
 </tr> 
</table>

Uma string vazia indica que essa camada não deve fornecer um mapa de imagem. A cadeia de caracteres deve ser corretamente codificada em HTTP para evitar problemas de análise.

Todos os caracteres de E comercial (&amp;) que ocorrem em *`string`* deve ser codificado em http.

Enquanto `mapA=` e `catalog::Map` especificar dados do mapa nas coordenadas da imagem de origem, `map=` assume as coordenadas de camada relativas ao canto superior esquerdo do retângulo da camada (após `rotate=` e `extend=` foram aplicados).

O mapa da imagem de saída é sempre recortado no retângulo da camada. Se a variável `shape` atributo é omitido ou definido como `default`, o retângulo da camada inteira será usado como a área do mapa da imagem.

## Propriedades {#section-a18d9ea95c71414a905a68b8839c0843}

Atributo de camada. Quando aplicado a `layer=comp`, os dados do mapa especificado são colocados atrás de todos os outros mapas de imagem. Ignorado, exceto `req=map`. Ignorado pelas camadas de efeito. `mapA=` é ignorado se `map=` também é especificado.

## Padrão {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` é usado se `map=` não foi especificado.

## Exemplo {#section-cd7691c94f984222845c86dcb0051ce8}

Defina um mapa de imagem retangular para uma camada de texto simples:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Um `AREA` o elemento com (em maioria) atributos padrão é usado para inserir a área do mapa para o retângulo de camada inteiro.

## Consulte também {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Mapas de imagem](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
