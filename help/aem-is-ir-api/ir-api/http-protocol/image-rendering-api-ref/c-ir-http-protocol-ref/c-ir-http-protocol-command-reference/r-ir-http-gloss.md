---
description: Luminosidade da superfície do material. Especifica o brilho relativo da superfície do material. Usado para selecionar o mapa de iluminação e controlar a renderização de efeitos de brilho e reflexos 3D.
seo-description: Luminosidade da superfície do material. Especifica o brilho relativo da superfície do material. Usado para selecionar o mapa de iluminação e controlar a renderização de efeitos de brilho e reflexos 3D.
seo-title: brilho
solution: Experience Manager
title: brilho
topic: Scene7 Image Serving - Image Rendering API
uuid: 3774e08b-d24e-4cf2-8719-32a21bb9bcb6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# brilho{#gloss}

Luminosidade da superfície do material. Especifica o brilho relativo da superfície do material. Usado para selecionar o mapa de iluminação e controlar a renderização de efeitos de brilho e reflexos 3D.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Brilho (0...100%) ou -1 para o valor de brilho padrão (referência). </p></td> 
 </tr> 
</table>

Valores de brilho mais altos normalmente causam reflexões mais fortes e mais nítidas e, se os efeitos de brilho estiverem ativados na vinheta, fortalece os realces especulares na superfície do material, principalmente aumentando o contraste da iluminação. Cada tipo de material ( `type=`) define um efeito de renderização mínimo e máximo. Para alguns tipos de materiais (por exemplo, papel de parede), `gloss=` quase não tem qualquer impacto no aspecto do efeito de renderização, enquanto para outros tipos de materiais (por exemplo, pedra ou cerâmica) o efeito é substancialmente mais pronunciado.

Se `illum=-1` a vinheta definir mapas de iluminação múltiplos, `gloss=` seleciona o mapa de iluminação usado para a operação de renderização atual. O renderizador escolhe o mapa de iluminação cujo valor de brilho é o mais próximo do brilho especificado.

`gloss=-1` seleciona o valor do brilho de referência do mapa de iluminação selecionado, conforme definido nas propriedades de visualização da vinheta. Isso garante que o mapa de iluminação seja usado exatamente como autoria, sem qualquer modificação adicional, mesmo que os efeitos de brilho estejam ativados. Se `illum=-1` também, utiliza-se o valor do brilho de referência do primeiro mapa de iluminação da visualização da vinheta.

## Propriedades {#section-92c20c7890fc4aad8d1725d1a1f82da6}

Atributo material. Ignorada se a vinheta não definir mapas de iluminação múltiplos ou se `illum=` for especificada, se a vinheta não incluir dados de reflexão 3D ou se o objeto atual não suportar reflexões 3D, ou se os efeitos de brilho estiverem desativados na vinheta.

## Padrão {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` se o material se basear numa entrada de catálogo, caso contrário o valor do brilho de referência do mapa de iluminação predefinido ou do mapa de iluminação especificado por `illum=`.

## Consulte também {#section-29f5b761481a4c52a499a2e16e63c70b}

[atributo::Brilho](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [tipo=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [bruto=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossário=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a), [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
