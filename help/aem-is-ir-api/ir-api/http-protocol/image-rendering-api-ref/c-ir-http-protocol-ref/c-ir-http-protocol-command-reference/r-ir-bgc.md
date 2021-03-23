---
description: Cor do plano de fundo. Especifica a cor subtrativa para texturas e decalques coloríveis.
seo-description: Cor do plano de fundo. Especifica a cor subtrativa para texturas e decalques coloríveis.
seo-title: bgc
solution: Experience Manager
title: bgc
uuid: 551a0da8-dd1f-484a-bf7e-f4896370340a
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---


# bgc{#bgc}

Cor do plano de fundo. Especifica a cor subtrativa para texturas e decalques coloríveis.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>Valor de cor cinza ou RGB. </p></td> 
 </tr> 
</table>

O algoritmo de colorização de textura da Renderização de imagem é bastante simples - os valores de componente de `bgc=` são subtraídos dos pixels de textura, `color=` é adicionado e, finalmente, o resultado é recortado para `0,0,0` e `255,255,255`.

Para usos típicos da coloração de textura, o valor de `bgc=` pode ser a cor mais importante ou dominante na imagem de textura. A Criação de imagens do Dynamic Media fornece ferramentas semiautomáticas que extraem valores de cores razoáveis `bgc=` das imagens de textura.

Quando um material de textura é aplicado a um objeto de vinheta não texturizável, `bgc=` é aplicado como a cor de primeiro plano se `color=` não for especificado.

## Propriedades {#section-b2db6f147d7f443ba9f671de04c2ef19}

Atributo de material. Ignorado por materiais de cor sólida e caixa.

## Padrão {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` se o material for baseado em uma entrada do catálogo, caso contrário  `bgc=808080` (cinza neutro).

## Exemplo {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Colorir um tecido de vestuário cuja textura tenha a cor RGB dominante 120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Consulte também {#section-de9958dd63a742b4b5d780c59a57da33}

[catálogo::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) ,  [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
