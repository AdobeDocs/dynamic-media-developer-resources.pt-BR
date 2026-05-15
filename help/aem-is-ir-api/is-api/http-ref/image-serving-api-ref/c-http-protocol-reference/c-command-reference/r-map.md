---
title: mapa
description: Dados do mapa de imagem. Fornece dados de mapa de imagem para esta camada. Substitui todos os dados do Mapa de catálogo para essa camada.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
TQID: 'https://experienceleague.adobe.com/9JJUVcw5-wl0B-rP-m6DC1c1DGIqxaV2UgboocFGGV8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 224
ht-degree: 0%

---

# mapa{#map}

Dados do mapa de imagem. Fornece dados de mapa de imagem para esta camada. Substitui todos os dados de catalog::Map dessa camada.

`map=[ *`cadeia`*]mapA=[ *`cadeiaA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cadeia de caracteres</span></span> </p></td> 
  <td class="stentry"> <p>Dados do mapa de imagem para esta camada em coordenadas de camada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>Dados do mapa de imagem para esta camada nas coordenadas da imagem de origem. </p></td> 
 </tr> 
</table>

Uma string vazia indica que essa camada não deve fornecer um mapa de imagem. A cadeia de caracteres deve ser corretamente codificada em HTTP para evitar problemas de análise.

Todos os caracteres de E comercial (&amp;) que ocorrem em *`string`* devem ser codificados em http.

Enquanto `mapA=` e `catalog::Map` especificam dados de mapa nas coordenadas da imagem de origem, `map=` assume coordenadas de camada relativas ao canto superior esquerdo do retângulo de camada (após `rotate=` e `extend=` serem aplicados).

O mapa da imagem de saída é sempre recortado no retângulo da camada. Se o atributo `shape` for omitido ou definido como `default`, o retângulo de camada inteiro será usado como a área do mapa de imagem.

## Propriedades {#section-a18d9ea95c71414a905a68b8839c0843}

Atributo de camada. Quando aplicados a `layer=comp`, os dados de mapa especificados são colocados atrás de todos os outros mapas de imagem. Ignorado, a menos que `req=map`. Ignorado pelas camadas de efeito. `mapA=` será ignorado se `map=` também for especificado.

## Padrão {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` será usado se `map=` não for especificado.

## Exemplo {#section-cd7691c94f984222845c86dcb0051ce8}

Defina um mapa de imagem retangular para uma camada de texto simples:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Um elemento `AREA` com (em maioria) atributos padrão é usado para inserir a área do mapa para o retângulo de camada inteiro.

## Consulte também {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Mapas de imagens](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
