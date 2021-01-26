---
description: Dados do mapa de imagem. Fornece dados de mapa de imagem para esta camada. Substitui todos os dados do mapa de catálogo para essa camada.
seo-description: Dados do mapa de imagem. Fornece dados de mapa de imagem para esta camada. Substitui todos os dados do mapa de catálogo para essa camada.
seo-title: mapa
solution: Experience Manager
title: mapa
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9c1c3323-21ab-4820-bf4e-761b82ada1ab
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---


# map{#map}

Dados do mapa de imagem. Fornece dados de mapa de imagem para esta camada. Substitui todos os dados do catálogo::Map para essa camada.

`map=[ *`string `*]mapA=[ *`A`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Dados do mapa de imagem para essa camada em coordenadas de camada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>Dados do mapa de imagem para essa camada em coordenadas de imagem de origem. </p></td> 
 </tr> 
</table>

Uma string vazia indica que essa camada não deve fornecer um mapa de imagem. A string deve ser corretamente codificada por HTTP para evitar problemas de análise.

Todos os caracteres de E comercial (&amp;) que ocorrem em *`string`* devem ser codificados por http.

Enquanto `mapA=` e `catalog::Map` especificam os dados do mapa nas coordenadas da imagem de origem, `map=` assume as coordenadas da camada relativas à parte superior esquerda do retângulo da camada (após `rotate=` e `extend=` terem sido aplicados).

O mapa de imagem de saída é sempre cortado no retângulo da camada. Se o atributo `shape` for omitido ou definido como `default`, todo o retângulo da camada será usado como área do mapa de imagem.

## Propriedades {#section-a18d9ea95c71414a905a68b8839c0843}

Atributo de camada. Quando aplicados a `layer=comp`, os dados do mapa especificados são dispostos em camadas atrás de todos os outros mapas de imagem. Ignorado a menos que `req=map`. Ignorado pelas camadas de efeito. `mapA=` é ignorada se também  `map=` for especificada.

## Padrão {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` é usada se não  `map=` for especificada.

## Exemplo {#section-cd7691c94f984222845c86dcb0051ce8}

Defina um mapa de imagem retangular para uma camada de texto simples:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Um elemento `AREA` com atributos padrão (principalmente) é usado para inserir a área do mapa para todo o retângulo da camada.

## Consulte também {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Mapas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab) de imagem,  [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
