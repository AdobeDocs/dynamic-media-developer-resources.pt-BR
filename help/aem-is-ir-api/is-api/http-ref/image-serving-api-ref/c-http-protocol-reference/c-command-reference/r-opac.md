---
description: Ajuste a opacidade da imagem. Permite diminuir a opacidade de primeiro plano de uma imagem, texto, cor sólida ou camada de efeito.
seo-description: Ajuste a opacidade da imagem. Permite diminuir a opacidade de primeiro plano de uma imagem, texto, cor sólida ou camada de efeito.
seo-title: opaco
solution: Experience Manager
title: opaco
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 268279bd-d777-4afe-b175-841af7e55406
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---


# opac{#opac}

Ajuste a opacidade da imagem. Permite diminuir a opacidade de primeiro plano de uma imagem, texto, cor sólida ou camada de efeito.

`opac= *``*[, *`opacityfillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> opacidade</span> </p> </td> 
  <td class="stentry"> <p>Opacidade primária (0...100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>Opacidade de preenchimento (0...100 int). </p></td> 
 </tr> 
</table>

A opacidade do primeiro plano para uma camada de imagem é determinada pela máscara de camada ou pelo canal alfa da imagem ou, se nenhum estiver presente, é de 100%. A opacidade de primeiro plano de uma camada de texto é 100% e a de uma camada de cor sólida é definida por `color=`.

`opac=` nunca modifica a opacidade das áreas preenchidas com  `color=` ou  `bgColor=`, exceto as áreas de primeiro plano das camadas de cor sólida e efeito (definidas com  `color=`).

Quando especificado em uma imagem, texto ou camada de cor sólida, *`opacity`* aplica a camada inteira, incluindo todas as camadas de efeito associadas, enquanto *`fillOpacity`* se aplica somente ao conteúdo da camada primária. Quando especificado em uma camada de efeito, *`opacity`* se aplica à camada de efeito, enquanto *`fillOpacity`* é ignorado.

A opacidade efetiva para o conteúdo da camada principal é ( *`opacity`* * *`fillOpacity`* / 100). A opacidade efetiva das camadas de efeito é (principal *`opacity`* * efeito *`opacity`* / 100).

## Propriedades {#section-ac3f136ff1584a2eab87500b7164f7fa}

Atributo de camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`.

## Padrão {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`, para que não haja alteração na opacidade da camada.

## Exemplo {#section-9710810e96af40538652e8ae4aadd3be}

... `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`...

A opacidade do texto neste exemplo é 90*70/100=63%, e a opacidade da camada de efeito é 90*50/100=45%.

## Consulte também {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
