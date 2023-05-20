---
description: Modo de repetição de textura. Especifica como as imagens de textura são lado a lado para preencher a superfície de destino.
solution: Experience Manager
title: Repetir
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d6946b0-a827-4ee6-963b-84529ad35ee9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 15%

---

# Repetir{#repeat}

Modo de repetição de textura. Especifica como as imagens de textura são lado a lado para preencher a superfície de destino.

## Propriedades {#section-cef4109cddf54ce095c3293d85bc412d}

Enum. Usado apenas para texturas repetíveis. Ignorado para todos os outros materiais.

Os seguintes valores são permitidos para materiais de textura repetíveis:

<table id="simpletable_C24FDA80A8AC431DA3FC86188E3774E1" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>0 </p></td> 
  <td class="- topic/stentry stentry"> <p>Repetição direta. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>1 </p></td> 
  <td class="- topic/stentry stentry"> <p>Lado a lado aleatório de 4 vias. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>2 </p></td> 
  <td class="- topic/stentry stentry"> <p>Lado a lado aleatório de 8 vias. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>3 </p></td> 
  <td class="- topic/stentry stentry"> <p>Lado a lado com diamante. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>4 </p></td> 
  <td class="- topic/stentry stentry"> <p>Papel de parede de um quarto de gota. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>5 </p></td> 
  <td class="- topic/stentry stentry"> <p>Papel de parede de terceira gota. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>6 </p></td> 
  <td class="- topic/stentry stentry"> <p>Meio-drop papel de parede pendurar. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>7 </p></td> 
  <td class="- topic/stentry stentry"> <p>Papel de parede de quinta gota pendurado. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>8 </p></td> 
  <td class="- topic/stentry stentry"> <p>Invertendo papel de parede pendurado. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>9 </p></td> 
  <td class="- topic/stentry stentry"> <p>Papel de parede aleatório pendurado. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>10 </p></td> 
  <td class="- topic/stentry stentry"> <p>Descarte aleatório. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>11 </p></td> 
  <td class="- topic/stentry stentry"> <p>Aleatória. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>12 </p></td> 
  <td class="- topic/stentry stentry"> <p>Meio a meio. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>13 </p></td> 
  <td class="- topic/stentry stentry"> <p>Espelho (bookmatch). </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>14 </p></td> 
  <td class="- topic/stentry stentry"> <p>Aleatório padrão. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>15 </p></td> 
  <td class="- topic/stentry stentry"> <p>Aleatório de alta frequência. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>16 </p></td> 
  <td class="- topic/stentry stentry"> <p>Aleatório de baixa frequência. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>17 </p></td> 
  <td class="- topic/stentry stentry"> <p>Aleatório horizontal. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>18 </p></td> 
  <td class="- topic/stentry stentry"> <p>Aleatório vertical. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>19 </p></td> 
  <td class="- topic/stentry stentry"> <p>O randomizador de borda. </p></td> 
 </tr> 
</table>

## Padrão {#section-23fba3bd1f3544c7913d12f2ca148517}

0 (repetição direta).

## Consulte também {#section-a08887a91db34ed3b183899c69c9f74f}

[repeat=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8)
