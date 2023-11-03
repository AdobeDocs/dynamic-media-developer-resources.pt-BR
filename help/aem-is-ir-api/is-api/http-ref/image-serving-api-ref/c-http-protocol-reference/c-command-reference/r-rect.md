---
title: rect
description: Retângulo de visão final. Ele permite que a imagem de visualização final seja desmontada em várias tiras ou blocos, que podem ser entregues separadamente e remontados pelo cliente sem problemas, sem artefatos ao longo das bordas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# rect{#rect}

Retângulo de visão final. Ele permite que a imagem de visualização final seja desmontada em várias tiras ou blocos, que podem ser entregues separadamente e remontados pelo cliente sem problemas, sem artefatos ao longo das bordas.

`rect= *`coord`*, *`tamanho`*[, *`escala`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Deslocamento em pixels do canto superior esquerdo da imagem da exibição para o canto superior esquerdo do retângulo de exibição (int, int), expresso em pixels, depois de <span class="varname"> escala</span> é aplicada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> tamanho</span> </p></td> 
  <td class="stentry"> <p>Tamanho do ROI em pixels (int, int). Especifica o tamanho da imagem de resposta. A imagem é preenchida com <span class="codeph"> bgc=</span> em áreas não cobertas pela imagem da exibição (ou transparente à esquerda, se <span class="codeph"> fmt=*-alpha</span> está presente na solicitação). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> escala</span> </p></td> 
  <td class="stentry"> <p>Fator de escala (real). Valores menores que 1,0 reduzem a resolução e valores maiores que 1,0 aumentam a resolução. </p></td> 
 </tr> 
</table>

Usando esse comando, o Servidor de imagens pode fornecer imagens grandes por meio de HTTP, que de outra forma excederia o limite de tamanho configurado com `attribute::MaxPix`.

>[!NOTE]
>
>Para obter melhores resultados, quando a compactação de JPEG é usada, o tamanho da faixa ou do bloco deve ser um múltiplo do tamanho do bloco de codificação de JPEG (16x16 pixels).

## Exemplo {#section-932fcfcb41d74a29bc929e4430c49601}

Separe uma imagem CMYK imprimível em várias tiras de resolução total para reduzir os tamanhos dos arquivos baixados. Se você solicitou uma imagem contígua:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

Em primeiro lugar, são obtidas informações relevantes sobre a imagem:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

A resposta de texto inclui estas propriedades:

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

Com base nessas informações, são desejadas quatro faixas de pixel de 600x2000. A variável `rect=` é usado para descrever os tamanhos e as posições das faixas.

Como essa imagem é alterada com frequência, a variável `id=` é incluído. Isso minimiza a chance de acabar com uma ou mais tiras de uma versão mais antiga da imagem que pode ter sido armazenada em cache em um CDN ou servidor proxy. O valor de `image.version` propriedade é usada para essa finalidade.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Propriedades {#section-aae223cee13e46d38b74680c048d945b}

Exibir atributo. Ela se aplica independentemente da configuração atual da camada.

Todas as áreas do ROI que se estendem para fora da imagem de exibição são preenchidas com `bgc=`.

Importante `rect=` é aplicado *após* escala final e ajuste com `scl=`, `wid=`, `hei=`, `fit=`, `rgn=`, e `align=`.

## Padrão {#section-b296d3bbfb19441f87137a452b70f19a}

Imagem de exibição inteira e não modificada ( `rect=0,0,width,height,1.0`).

## Consulte Também {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [estender=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5), [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
