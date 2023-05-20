---
title: bgc
description: Cor de fundo. Especifica a cor subtrativa para texturas e decalques coloridos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# bgc {#bgc}

Cor de fundo. Especifica a cor subtrativa para texturas e decalques coloridos.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> cor</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>valor da cor RGB ou cinza. </p></td> 
 </tr> 
</table>

O algoritmo de colorização de textura da Renderização de imagem é simples - os valores do componente de `bgc=` são subtraídos dos valores dos pixels de textura; `color=` é adicionado e, por fim, o resultado é recortado para `0,0,0` e `255,255,255`.

Para usos típicos de colorização de textura, o valor de `bgc=` pode ser a cor mais importante ou dominante na imagem de textura. O Dynamic Media Image Authoring fornece ferramentas semiautomáticas que extraem informações `bgc=` valores de cor de imagens de texturas.

Quando um material de textura é aplicado a um objeto de vinheta não texturável, `bgc=` é aplicada como a cor do primeiro plano se `color=` não foi especificado.

## Propriedades {#section-b2db6f147d7f443ba9f671de04c2ef19}

Atributo de material. Ignorado por materiais de gabinete e cores sólidas.

## Padrão {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` Se o material for baseado em uma entrada de catálogo, caso contrário `bgc=808080` (cinza neutro).

## Exemplo {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Colorir um tecido de vestuário cuja textura tenha a cor de RGB dominante 120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Consulte também {#section-de9958dd63a742b4b5d780c59a57da33}

[catálogo::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
