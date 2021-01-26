---
description: Uso da máscara de imagem. Especifica como a máscara ou o canal alfa da imagem é usado para operações na imagem (por exemplo, colorizar=). Quando especificado em uma camada de efeito, permite aplicar o efeito à área de plano de fundo da camada pai ou a todo o retângulo da camada pai.
seo-description: Uso da máscara de imagem. Especifica como a máscara ou o canal alfa da imagem é usado para operações na imagem (por exemplo, colorizar=). Quando especificado em uma camada de efeito, permite aplicar o efeito à área de plano de fundo da camada pai ou a todo o retângulo da camada pai.
seo-title: maskUse
solution: Experience Manager
title: maskUse
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 2c70da87-f869-495a-be50-226a4516e002
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# maskUse{#maskuse}

Uso da máscara de imagem. Especifica como a máscara ou o canal alfa da imagem é usado para operações na imagem (por exemplo, colorizar=). Quando especificado em uma camada de efeito, permite aplicar o efeito à área de plano de fundo da camada pai ou a todo o retângulo da camada pai.

`maskUse=norm|invert|off`

A tabela a seguir ilustra o efeito de `maskUse=` dependendo da disponibilidade e do tipo da máscara (canal alfa) associada à imagem da camada.

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Valor</b> </th> 
   <th class="entry"> <b> Sem máscara</b> </th> 
   <th class="entry"> <b> Alfa não associado (ou imagem de máscara separada)</b> </th> 
   <th class="entry"> <b> Alfa associado (pré-multiplicado)</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> off  </span> </p> </td> 
   <td> <p> Retângulo de imagem opaco </p> </td> 
   <td> <p> Retângulo de imagem opaco </p> </td> 
   <td> <p> Área de primeiro plano da imagem sobre o retângulo preenchido com preto sólido </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> norma  </span> </p> </td> 
   <td> <p> Retângulo de imagem opaco </p> </td> 
   <td> <p> Área de primeiro plano da imagem </p> </td> 
   <td> <p> Área de primeiro plano da imagem ou da camada </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> inverter  </span> </p> </td> 
   <td> <p> Camada oculta </p> </td> 
   <td> <p> Área de plano de fundo da imagem </p> </td> 
   <td> <p> Área de plano de fundo da imagem ou camada preenchida com preto sólido </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f36ad1af348e45aeb3eb336544df30b0}

Imagem ou atributo de camada. Aplica-se à camada 0 se `layer=comp`. Se especificado em uma camada de efeito, o comando modifica a máscara herdada da camada pai.

O comportamento de `maskUse=` não é definido e não é suportado quando especificado com camadas de texto ou cores sólidas quando nenhuma máscara de imagem é aplicável (especificado com `mask=` ou `catalog::Mask`).

## Padrão {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## Exemplo {#section-daa371e9be5547368ff6772342acba0a}

Colorir a área de plano de fundo de uma imagem; o primeiro plano da imagem é definido por uma imagem de máscara separada. Isso é feito colocando o plano de fundo da imagem colorida na parte superior se a imagem não modificada:

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## Consulte também {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
