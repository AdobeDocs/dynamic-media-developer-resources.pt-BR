---
title: alinhar
description: Alinhar imagem com exibição. Alinha a imagem composta (possivelmente após o dimensionamento, se scl= também for especificado) no retângulo de exibição definido por wid= e hei=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# alinhar{#align}

Alinhar imagem com exibição. Alinha a imagem composta (possivelmente após o dimensionamento, se scl= também for especificado) no retângulo de exibição definido por wid= e hei=.

` align= *`horiz`*, *`vert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz </span> </span> </p> </td> 
  <td class="stentry"> <p>alinhamento horizontal (real, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span> </span> </p> </td> 
  <td class="stentry"> <p>alinhamento vertical (real, -1.0...1.0) </p> </td> 
 </tr> 
</table>

Especifique `align=-1,-1` para alinhar o canto superior esquerdo da imagem composta com o canto superior esquerdo da exibição. Especifique `align=1,1` para alinhar o canto inferior direito da imagem com o canto inferior direito da exibição. Para solicitações de imagem e miniatura padrão, qualquer área da exibição que não é coberta pelos dados de imagem composta é preenchida com `bgc=`.

## Propriedades {#section-3fbec8206fc944eda4746d8be84f3b41}

Exibir atributo. ( `align=` também é usado para definir o alinhamento entre uma imagem de marca d&#39;água e a imagem composta à qual a marca d&#39;água é aplicada.) Aplica-se independentemente da configuração atual da camada. Ignorado se apenas um de `wid=` e `hei=` for especificado e quando `fit=constrain` ou `fit=stretch`.

## Padrão {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, que centraliza a imagem no retângulo de exibição.

## Exemplo {#section-2c9447aa2e184fb8ab1a4370dc61d554}

A solicitação a seguir cabe `myImage` em um retângulo de exibição de 200x200 pixels.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Se `myImage` for exatamente quadrado, ele preencherá o retângulo de exibição inteiro. Se `myImage` tiver uma proporção de retrato, ela será dimensionada para ter 200 pixels de altura e centralizada horizontalmente na exibição. Se `myImage` tiver uma taxa de proporção de paisagem, ela será dimensionada para ter 200 pixels de largura e será alinhada à borda superior da exibição. Em todos os casos, a imagem retornada tem exatamente 200x200 pixels de tamanho; qualquer espaço não coberto pelo `myImage` dimensionado é preenchido com `attribute::BkgColor` (especifique bgc= para controlar a cor do plano de fundo dinamicamente).

## Consulte também {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Marcas d&#39;água](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
