---
title: sub
description: Subseleção. Permite aplicar diferentes materiais a diferentes áreas do objeto ou grupo selecionado e remover materiais aplicados anteriormente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9968fbb-c38b-4180-81be-19992fa8f347
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 4%

---

# sub{#sub}

Subseleção. Permite aplicar diferentes materiais a diferentes áreas do objeto ou grupo selecionado e remover materiais aplicados anteriormente.

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
  <td class="stentry"> <p>Selecione a área da borda da parede do meio. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Selecione a área da borda inferior da parede. </p> </td> 
 </tr> 
</table>

Atualmente suportado apenas para objetos da parede. Encerra um MSS anterior e inicia um novo MSS para o material a ser aplicado à subseleção especificada.

Um material especificado para a parede superior ou inferior aplica-se a toda a parede, a menos que um material diferente para a outra metade da parede também tenha sido especificado.

## Propriedades {#section-b202139d6d0847cc8d520a154104ab9d}

Comando de seleção; delimitador de MSS.

## Padrão {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## Consulte também {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
