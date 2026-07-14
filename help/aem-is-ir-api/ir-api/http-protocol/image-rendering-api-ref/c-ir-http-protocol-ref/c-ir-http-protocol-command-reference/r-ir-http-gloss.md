---
title: brilho
description: Brilho da superfície do material. Especifica a luminosidade relativa da superfície do material. Usado para selecionar o mapa de iluminação e controlar a renderização de efeitos de brilho e reflexos 3D.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
TQID: 'https://experienceleague.adobe.com/-69G38JBpD4-X1wvkFtfvvZpdbHs7pcPiHnbNDgGRCA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 314
ht-degree: 0%

---

# brilho{#gloss}

Brilho da superfície do material. Especifica a luminosidade relativa da superfície do material. Usado para selecionar o mapa de iluminação e controlar a renderização de efeitos de brilho e reflexos 3D.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Brilho (0 a 100%) ou -1 para o valor de brilho padrão (referência). </p></td> 
 </tr> 
</table>

Valores de brilho mais altos normalmente causam reflexões mais fortes e nítidas e, se os efeitos de brilho estiverem ativados na vinheta, fortalece os realces especulares na superfície do material, principalmente aumentando o contraste da iluminação. Cada tipo de material ( `type=`) define um efeito de renderização mínimo e máximo. Para alguns tipos de material (por exemplo, papel de parede), `gloss=` tem impacto mínimo na aparência do efeito de renderização, enquanto para outros tipos de material (por exemplo, pedra ou cerâmica), o efeito é substancialmente mais pronunciado.

Se `illum=-1` e a vinheta definir vários mapas de iluminação, `gloss=` selecionará o mapa de iluminação usado para a operação de renderização atual. O renderizador escolhe o mapa de iluminação cujo valor de brilho está mais próximo do brilho especificado.

`gloss=-1` Seleciona o valor de brilho de referência do mapa de iluminação selecionado, conforme definido nas propriedades de exibição da vinheta. Esse valor garante que o mapa de iluminação seja usado exatamente como foi criado, sem modificações adicionais, mesmo se os efeitos de brilho estiverem ativados. Se `illum=-1` então o valor de brilho de referência do primeiro mapa de iluminação na visão da vinheta é usado.

## Propriedades {#section-92c20c7890fc4aad8d1725d1a1f82da6}

Atributo de material. Ignorado se a vinheta não definir vários mapas de iluminação. Ou, se `illum=` for especificado, se a vinheta não incluir dados de reflexão 3D. Ou, se o objeto atual não suportar reflexões 3D ou se os efeitos de brilho estiverem desativados na vinheta.

## Padrão {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` Se o material for baseado em uma entrada do catálogo, caso contrário, o valor do brilho de referência do mapa de iluminação padrão ou do mapa de iluminação especificado por `illum=`.

## Consulte também {#section-29f5b761481a4c52a499a2e16e63c70b}

[atributo::Brilho](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [tipo=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [bruto=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a), [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)

