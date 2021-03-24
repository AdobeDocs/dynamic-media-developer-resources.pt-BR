---
description: Transformação de perspectiva. Aplique uma transformação de perspectiva à imagem de origem da camada para preencher a região especificada com o quadrilateral. Outras áreas da camada permanecem transparentes.
solution: Experience Manager
title: perspectiva
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---


# perspectiva{#perspective}

Transformação de perspectiva. Aplique uma transformação de perspectiva à imagem de origem da camada para preencher a região especificada com o quadrilateral. Outras áreas da camada permanecem transparentes.

`perspective= *``*[, *`perspQuadresOptions`*]`

`perspectiveN= *``*[, *`perspQuadNresOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>Coordenadas de pixel quadrilateral de perspectiva (8 reais, separados por vírgulas). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>Coordenadas normalizadas quadrilaterais de perspectiva (8 reais, separados por vírgulas). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>Opções de nova amostra (veja abaixo). </p></td> 
 </tr> 
</table>

*`perspQuad`* consiste em quatro valores de coordenadas de pixel no espaço de coordenadas composto (ou camada 0), originado no canto superior esquerdo da imagem composta.

`perspQuadN` consiste em quatro valores de coordenadas normalizados, onde  `0.0,0.0` corresponde ao canto superior esquerdo da imagem composta/camada 0 e  `1.0,1.0` ao canto inferior direito.

A imagem de entrada é transformada de forma que o canto superior esquerdo da imagem de entrada mapeie para o primeiro valor de coordenada `perspQuad[N]`, o canto superior direito para a segunda coordenada, o canto inferior direito para a terceira coordenada e o canto inferior esquerdo para a quarta coordenada.

>[!NOTE]
>
>`pos=` pode ser usada para posicionar ainda mais a camada transformada na imagem composta.

As coordenadas quadrilaterais da perspectiva podem estar localizadas fora da imagem composta.

O comportamento é indefinido se o quadrilateral não for adequado para uma transformação de perspectiva (por exemplo, se dois ou mais vértices coincidirem, se três ou todos os vértices estiverem na mesma linha, ou se o quadrilateral for autointersetante ou côncavo).

## Considerações de qualidade {#section-7cc9056afa614300a9b8844d39739fc3}

Embora a implementação padrão produza um compromisso razoável entre qualidade e desempenho, às vezes pode ser necessário aumentar a resolução da imagem de origem para melhorar a nitidez ou reduzi-la para reduzir os artefatos de aliasing.

Se a fonte for uma imagem, use `scale=` para escolher uma resolução diferente (relativa à resolução completa da imagem). O valor `scale=` especificado é arredondado para o próximo nível de resolução PTIF mais alto. No caso de uma fonte de solicitação aninhada, o tamanho da imagem produzida pela solicitação aninhada pode ser ajustado para alcançar a nitidez desejada. Para camadas de texto, a resolução da imagem de entrada (o texto renderizado) é ajustada selecionando um tamanho= valor maior junto com o aumento da resolução especificada com `textAttr=`.

*`resOptions`* permite selecionar um algoritmo de reamostragem alternativo. Os seguintes valores são suportados (diferencia maiúsculas de minúsculas):

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
   <td> <p> Mais próximo. </p> </td> 
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
   <td> <p> <span class="codeph">R3<span class="varname"> Tn</span></span> </p> </td> 
   <td> <p> A superamostragem com tremulação ajustável (<span class="varname"> n</span> deve ser um valor inteiro entre 0 e 200). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-818e57df0a1b4449888543bc6af77751}

comando Camada. Aplica-se à camada atual ou à camada 0, se `layer=comp`. Ignorado por camadas de efeito.

`res=` é sempre ignorada quando a perspectiva está presente na mesma camada. `size=` é ignorada quando especificada para camadas de imagem. `size=` e  `res=` em camadas com  `perspective=` são reservadas para uso futuro.

## Padrão {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, sem transformação de perspectiva.

## Consulte também {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) ,  [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065),  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
