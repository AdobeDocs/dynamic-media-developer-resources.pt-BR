---
title: sel
description: Selecione o objeto por localização de pixel.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---

# sel{#sel}

Selecione o objeto por localização de pixel.

` sel= *`x`*, *`y`*[, *`nível`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>Escolha as coordenadas de localização em pixels (int, int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nível </span> </p> </td> 
  <td class="stentry"> <p>Nível do grupo (int). </p> </td> 
 </tr> 
</table>

Seleciona o grupo ou objeto nas coordenadas de pixel especificadas por *`x, y`* e inicia um novo MSS. Se nenhum objeto selecionável estiver no local de separação ou se o local de separação não for válido, a ação especificada por `attribute::OnFailSel` for tomada.

*`level`* Especifica se é necessário selecionar o grupo mais externo ou detalhar para um grupo ou objeto aninhado. If *`level`* não especificado, o grupo mais externo é selecionado. Defina como 1 para selecionar um nível de grupo abaixo do grupo mais externo. Defina como um número grande (como 99) para selecionar o objeto ou grupo mais próximo selecionável.

## Propriedades {#section-8f27e84d88734a62a5e398e0c9972bdc}

comando Seleção; Delimitador MSS. A seleção de objeto é persistente até que outro objeto seja selecionado, com `obj=` ou `sel=`.

*`x, y`* Deve estar no intervalo 0, 0 (canto superior esquerdo da imagem) para *`wid`*-1, *`hei`*-1 (parte inferior, canto direito da imagem), em que *`wid`* e *`hei`* é o tamanho da exibição de vinheta não dimensionada.

Se especificado, *`level`* deve ser 0 ou maior.

## Padrão {#section-e13c705a3e76468894b4ec190ed8a893}

Nenhum para *`x, y`*. *`level`* O padrão é 0.

## Consulte também {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [atributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [atributo::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
