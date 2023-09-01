---
title: perspectiva
description: Transformação em perspectiva. Aplique uma transformação de perspectiva à imagem de origem da camada para que ela preencha a região especificada com o quadrilátero. Outras áreas da camada permanecem transparentes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# perspectiva{#perspective}

Transformação em perspectiva. Aplique uma transformação de perspectiva à imagem de origem da camada para que ela preencha a região especificada com o quadrilátero. Outras áreas da camada permanecem transparentes.

`perspective= *`perspQuad`*[, *`resOptions`*]`

`perspectiveN= *`perspQuadN`*[, *`resOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>Coordenadas de pixel quadrilateral de perspectiva (8 reais, separados por vírgulas). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>Perspectiva quadrilateral coordenadas normalizadas (8 reais, separados por vírgulas). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>Opções de reamostragem (veja abaixo). </p></td> 
 </tr> 
</table>

O modificador *`perspQuad`* consiste em quatro valores de coordenadas de pixel no espaço de coordenadas composto (ou camada 0), que se origina no canto superior esquerdo da imagem composta.

O modificador `perspQuadN` consiste em quatro valores de coordenadas normalizados, onde `0.0,0.0` corresponde ao canto superior esquerdo da imagem composta/camada 0 e `1.0,1.0` para o canto inferior direito.

A imagem de entrada é transformada de modo que o canto superior esquerdo da imagem de entrada mapeie para o primeiro valor de coordenada de `perspQuad[N]`, o canto superior direito para a segunda coordenada, o canto inferior direito para a terceira coordenada e o canto inferior esquerdo para a quarta coordenada.

>[!NOTE]
>
>O modificador `pos=` para posicionar ainda mais a camada transformada na imagem composta.

As coordenadas quadrilaterais da perspectiva podem estar localizadas fora da imagem composta.

O comportamento é indefinido se o quadrilátero não for adequado para uma transformação de perspectiva. Por exemplo, se dois ou mais vértices coincidem, se três ou todos os vértices estão na mesma linha, ou se o quadrilátero é autointerseção ou côncavo.

## Considerações de qualidade {#section-7cc9056afa614300a9b8844d39739fc3}

Embora a implementação padrão produza um compromisso razoável entre qualidade e desempenho, pode ser necessário aumentar a resolução da imagem de origem para melhorar a nitidez ou reduzi-la para reduzir artefatos de suavização.

Se a origem for uma imagem, use `scale=` para escolher uma resolução diferente (relativa à resolução total da imagem). O especificado `scale=` é arredondado para o próximo nível superior de resolução de PTIF. Se houver uma fonte de solicitação aninhada, o tamanho da imagem produzida pela solicitação aninhada poderá ser ajustado para atingir a nitidez desejada. Para camadas de texto, a resolução da imagem de entrada (o texto renderizado) é ajustada selecionando-se um valor maior size= com o aumento da resolução especificada com `textAttr=`.

O modificador *`resOptions`* permite selecionar um algoritmo alternativo de reamostragem. Os seguintes valores são suportados (distinção entre maiúsculas e minúsculas):

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Valor</b> </th> 
   <th class="entry"> <b> Descrição</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> Vizinho mais próximo. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> Bi-linear. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> Superamostragem padrão (padrão). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> Superamostragem com variação ajustável (<span class="varname"> n</span> deve ser um valor inteiro de 0 a 200). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-818e57df0a1b4449888543bc6af77751}

Camada. Se aplica à camada atual ou à camada 0 `layer=comp`. Ignorado pelas camadas de efeito.

O modificador `res=` é sempre ignorado quando a perspectiva está presente na mesma camada. O modificador `size=` é ignorado quando especificado para camadas de imagem. Os modificadores `size=` e `res=` em camadas com `perspective=` são reservados para uso futuro.

## Padrão {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, para nenhuma transformação de perspectiva.

## Consulte também {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
