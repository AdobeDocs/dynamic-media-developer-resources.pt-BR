---
description: Subseleção. Permite aplicar materiais diferentes a diferentes áreas do objeto ou grupo selecionado, bem como remover materiais aplicados anteriormente.
seo-description: Subseleção. Permite aplicar materiais diferentes a diferentes áreas do objeto ou grupo selecionado, bem como remover materiais aplicados anteriormente.
seo-title: sub
solution: Experience Manager
title: sub
topic: Scene7 Image Serving - Image Rendering API
uuid: cb9f4dc5-9d89-483a-ae72-b9076b27c57e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# sub{#sub}

Subseleção. Permite aplicar materiais diferentes a diferentes áreas do objeto ou grupo selecionado, bem como remover materiais aplicados anteriormente.

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Selecione a parede inteira. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Selecione a metade superior da parede. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Selecione a metade inferior da parede. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Selecione a área superior da borda da parede. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Selecione a área da borda da parede central. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Selecione a área da borda inferior da parede. </p> </td> 
 </tr> 
</table>

Atualmente, há suporte apenas para objetos de parede. Encerra um MSS anterior e start um novo MSS para o material a ser aplicado à subseleção especificada.

Um material especificado para a parede superior ou inferior será aplicado a toda a parede, a menos que também tenha sido especificado um material diferente para a outra metade da parede.

## Propriedades {#section-b202139d6d0847cc8d520a154104ab9d}

comando Seleção; Delimitador MSS.

## Padrão {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## Consulte também {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
