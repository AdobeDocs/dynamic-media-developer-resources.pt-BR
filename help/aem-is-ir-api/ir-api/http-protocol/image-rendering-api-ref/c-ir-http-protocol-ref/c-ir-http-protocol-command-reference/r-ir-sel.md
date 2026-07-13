---
title: sel
description: Selecionar objeto por localização de pixel.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
TQID: 'https://experienceleague.adobe.com/nmXZZFxdpxJTY4j12JRyhCe-sOZIjajFSfzmPId9X3g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# sel{#sel}

Selecionar objeto por localização de pixel.

` sel= *`x`*, *`y`*[, *`level`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x, y </span> </p> </td> 
  <td class="stentry"> <p>Coletar coordenadas de localização em pixels (int, int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nível </span> </p> </td> 
  <td class="stentry"> <p>Nível de grupo (int). </p> </td> 
 </tr> 
</table>

Seleciona o grupo ou objeto nas coordenadas em pixels especificadas por *`x, y`* e inicia um novo MSS. Se nenhum objeto selecionável estiver no local de separação, ou se o local de separação não for válido, a ação especificada por `attribute::OnFailSel` será executada.

*`level`* Especifica se o grupo mais externo deve ser selecionado ou se deve ser feito o drill-down para um grupo ou objeto aninhado. Se *`level`* não for especificado, o grupo mais externo será selecionado. Defina como 1 para selecionar um nível de grupo abaixo do grupo mais externo. Defina como um número grande (como 99) para selecionar o objeto ou grupo que pode ser selecionado mais interno.

## Propriedades {#section-8f27e84d88734a62a5e398e0c9972bdc}

Comando de seleção; delimitador de MSS. A seleção de objeto é persistente até que outro objeto seja selecionado, com `obj=` ou `sel=`.

*`x, y`* Deve estar no intervalo de 0, 0 (canto superior esquerdo da imagem) a *`wid`*-1, *`hei`*-1 (canto inferior direito da imagem), onde *`wid`* e *`hei`* é o tamanho da exibição de vinheta não dimensionada.

Se especificado, *`level`* deve ser 0 ou maior.

## Padrão {#section-e13c705a3e76468894b4ec190ed8a893}

Nenhum para *`x, y`*. *`level`* O padrão é 0.

## Consulte também {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [atributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [atributo::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)

