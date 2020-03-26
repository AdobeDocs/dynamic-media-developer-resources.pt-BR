---
description: Alinhar imagem à Visualização. Alinha a imagem composta (possivelmente após redimensionamento, se scl= também for especificado) dentro do retângulo de visualização definido por wid= e hei=.
seo-description: Alinhar imagem à Visualização. Alinha a imagem composta (possivelmente após redimensionamento, se scl= também for especificado) dentro do retângulo de visualização definido por wid= e hei=.
seo-title: alinhar
solution: Experience Manager
title: alinhar
topic: Scene7 Image Serving - Image Rendering API
uuid: 91940bd4-8e2b-4949-a76d-31cd238783bc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# alinhar{#align}

Alinhar imagem à Visualização. Alinha a imagem composta (possivelmente após redimensionamento, se scl= também for especificado) dentro do retângulo de visualização definido por wid= e hei=.

` align= *``*, *`horizontal`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cavalo </span></span> </p> </td> 
  <td class="stentry"> <p>alinhamento horizontal (real, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span></span> </p> </td> 
  <td class="stentry"> <p>alinhamento vertical (real, -1.0...1.0) </p> </td> 
 </tr> 
</table>

Especifique `align=-1,-1` para alinhar a parte superior esquerda da imagem composta com a parte superior esquerda da visualização, especifique `align=1,1` para alinhar a parte inferior direita da imagem com a parte inferior direita da visualização. Para solicitações padrão de imagem e miniatura, qualquer área da visualização que não seja coberta por dados de imagem composta é preenchida com `bgc=`.

## Propriedades {#section-3fbec8206fc944eda4746d8be84f3b41}

Atributo de Visualização. (também `align=` é usado para definir o alinhamento entre uma imagem de marca d&#39;água e a imagem composta à qual a marca d&#39;água é aplicada.) Aplica-se independentemente da configuração de camada atual. Ignorado se apenas um de `wid=` e `hei=` for especificado e quando `fit=constrain` ou `fit=stretch`.

## Padrão {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, que centraliza a imagem no retângulo da visualização.

## Example {#section-2c9447aa2e184fb8ab1a4370dc61d554}

A solicitação a seguir se encaixa `myImage` em um retângulo de visualização de 200 x 200 pixels.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Se `myImage` for exatamente quadrado, preencherá todo o retângulo visualização. Se `myImage` tiver uma proporção retrato, ela será dimensionada para ter 200 pixels de altura e será centralizada horizontalmente na visualização. Se `myImage` tiver uma proporção paisagem, ela será dimensionada para ter 200 pixels de largura e será alinhada à borda superior da visualização. Em todos os casos, a imagem retornada tem exatamente 200 x 200 pixels de tamanho; qualquer espaço não coberto pela escala `myImage` é preenchido com `attribute::BkgColor` (especifique bgc= para controlar dinamicamente a cor do plano de fundo).

## Consulte também {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Marcas d&#39;água](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
