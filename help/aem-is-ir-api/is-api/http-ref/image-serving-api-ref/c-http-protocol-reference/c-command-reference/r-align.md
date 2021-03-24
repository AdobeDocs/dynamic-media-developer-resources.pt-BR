---
description: Alinhe a imagem com a exibição. Alinha a imagem composta (possivelmente após o dimensionamento, se scl= também for especificado) dentro do retângulo de exibição definido por wid= e hei=.
solution: Experience Manager
title: alinhar
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# align{#align}

Alinhe a imagem com a exibição. Alinha a imagem composta (possivelmente após o dimensionamento, se scl= também for especificado) dentro do retângulo de exibição definido por wid= e hei=.

` align= *``*, *`horizontal`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cavalo  </span> </span> </p> </td> 
  <td class="stentry"> <p>alinhamento horizontal (real, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert  </span> </span> </p> </td> 
  <td class="stentry"> <p>alinhamento vertical (real, -1.0...1.0) </p> </td> 
 </tr> 
</table>

Especifique `align=-1,-1` para alinhar a parte superior esquerda da imagem composta com a parte superior esquerda da exibição, especifique `align=1,1` para alinhar a parte inferior, direita da imagem com a parte inferior direita da exibição. Para solicitações padrão de imagem e miniatura, qualquer área da exibição que não seja coberta por dados de imagem composta é preenchida com `bgc=`.

## Propriedades {#section-3fbec8206fc944eda4746d8be84f3b41}

Exibir atributo. ( `align=` também é usado para definir o alinhamento entre uma imagem de marca d&#39;água e a imagem composta à qual a marca d&#39;água é aplicada.) Aplica-se independentemente da configuração de camada atual. Ignorado se apenas um de `wid=` e `hei=` for especificado e quando `fit=constrain` ou `fit=stretch` for especificado.

## Padrão {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, que centraliza a imagem no retângulo de exibição.

## Exemplo {#section-2c9447aa2e184fb8ab1a4370dc61d554}

A solicitação a seguir se encaixa `myImage` em um retângulo de exibição de 200x200 pixels.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Se `myImage` for exatamente quadrado, preencherá o retângulo de exibição inteiro. Se `myImage` tiver uma taxa de proporção do retrato, ela será dimensionada para ter 200 pixels de altura e será centralizada horizontalmente na exibição. Se `myImage` tiver uma taxa de aspecto paisagem, ela será dimensionada para ter 200 pixels de largura e será alinhada à borda superior da exibição. Em todos os casos, a imagem retornada tem exatamente 200x200 pixels de tamanho; qualquer espaço não coberto pelo dimensionado `myImage` é preenchido com `attribute::BkgColor` (especifique bgc= para controlar dinamicamente a cor do plano de fundo).

## Consulte também {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [marcas d&#39;água](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
