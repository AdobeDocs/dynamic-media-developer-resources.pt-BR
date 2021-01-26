---
description: Retângulo de visualização final. Permite que a imagem de visualização final seja desmontada em várias faixas ou blocos, que podem ser entregues separadamente e remontados pelo cliente perfeitamente, sem artefatos ao longo das bordas.
seo-description: Retângulo de visualização final. Permite que a imagem de visualização final seja desmontada em várias faixas ou blocos, que podem ser entregues separadamente e remontados pelo cliente perfeitamente, sem artefatos ao longo das bordas.
seo-title: rect
solution: Experience Manager
title: rect
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c4830fc5-d102-4789-8753-0a660d4a557e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---


# rect{#rect}

Retângulo de visualização final. Permite que a imagem de visualização final seja desmontada em várias faixas ou blocos, que podem ser entregues separadamente e remontados pelo cliente perfeitamente, sem artefatos ao longo das bordas.

`rect= *``*, *``*[, *`cordsizescale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cabo</span> </p> </td> 
  <td class="stentry"> <p>O deslocamento de pixel do canto superior esquerdo da imagem de visualização para a parte superior esquerda do retângulo de visualização (int, int), expresso em pixels, depois que <span class="varname"> scale</span> é aplicado. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> tamanho</span> </p></td> 
  <td class="stentry"> <p>Tamanho do ROI em pixels (int, int). Especifica o tamanho da imagem de resposta. A imagem é preenchida com <span class="codeph"> bgc=</span> em áreas não cobertas pela imagem de visualização (ou transparente à esquerda, se <span class="codeph"> fmt=*-alfa</span> estiver presente na solicitação). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> escala</span> </p></td> 
  <td class="stentry"> <p>Fator de escala (real). Valores menores que 1,0 reduzem a resolução e valores maiores que 1,0 aumentam a resolução. </p></td> 
 </tr> 
</table>

Usando esse comando, o Serviço de Imagens pode fornecer imagens grandes via HTTP, o que, de outra forma, excederia o limite de tamanho configurado com `attribute::MaxPix`.

>[!NOTE]
>
>Para obter melhores resultados quando a compactação JPEG é usada, o tamanho da fita ou do bloco deve ser um múltiplo do tamanho do bloco de codificação JPEG (16x16 pixels).

## Exemplo {#section-932fcfcb41d74a29bc929e4430c49601}

Separe uma imagem CMYK imprimível em várias faixas de resolução completa para reduzir os tamanhos de arquivos de download. Se solicitássemos uma imagem contígua:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

Em primeiro lugar, são obtidas informações relevantes sobre a imagem:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

A resposta de texto inclui estas propriedades:

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

Com base nessas informações, decidimos que queremos quatro faixas de 600 x 2000 pixels. O comando `rect=` é usado para descrever os tamanhos e as posições da película.

Como essa imagem é alterada com frequência, incluiremos o comando `id=` para minimizar a chance de que acabemos com uma ou mais faixas de uma versão mais antiga da imagem que possam ter sido armazenadas em cache em um CDN ou servidor proxy. O valor da propriedade `image.version` é usado para essa finalidade.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Propriedades {#section-aae223cee13e46d38b74680c048d945b}

Atributo de visualização. Aplica-se independentemente da configuração de camada atual.

Qualquer área do ROI que se estende fora da imagem da visualização é preenchida com `bgc=`.

`rect=` importante é aplicado *depois de* escala final e ajuste com `scl=`, `wid=`, `hei=`, `fit=`, `rgn=` e `align=`.

## Padrão {#section-b296d3bbfb19441f87137a452b70f19a}

Imagem de visualização inteira e não modificada ( `rect=0,0,width,height,1.0`).

## Consulte Também {#section-74015202c0c545ec82aec614d74b4bbd}

[safça=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [estende=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)  [ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)  [, alinhamento=, fit=, rgn=, Atributo::MaxPix, id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
