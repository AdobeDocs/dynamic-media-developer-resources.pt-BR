---
description: Modo de repetição de textura. Especifica como as imagens de textura são unidas para preencher a superfície de destino.
seo-description: Modo de repetição de textura. Especifica como as imagens de textura são unidas para preencher a superfície de destino.
seo-title: Repetir
solution: Experience Manager
title: Repetir
uuid: bd15a573-9902-4672-992d-90d171160a46
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 13%

---


# Repetir{#repeat}

Modo de repetição de textura. Especifica como as imagens de textura são unidas para preencher a superfície de destino.

## Propriedades {#section-cef4109cddf54ce095c3293d85bc412d}

Enum. Usado apenas para texturas repetíveis. Ignorado para todos os outros materiais.

São permitidos os seguintes valores para os materiais de textura repetíveis:

<table id="simpletable_C24FDA80A8AC431DA3FC86188E3774E1" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>0 </p></td> 
  <td class="- topic/stentry stentry"> <p>Repetição direta. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>3 </p></td> 
  <td class="- topic/stentry stentry"> <p>Otimização aleatória de 4 vias. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>2 </p></td> 
  <td class="- topic/stentry stentry"> <p>Otimização aleatória de 8 vias. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>3 </p></td> 
  <td class="- topic/stentry stentry"> <p>Lado a lado. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>4 </p></td> 
  <td class="- topic/stentry stentry"> <p>Suspensão do papel de parede. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>5 </p></td> 
  <td class="- topic/stentry stentry"> <p>Travamento do papel de parede de terceira gota. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>6 </p></td> 
  <td class="- topic/stentry stentry"> <p>Travamento de papel de parede com meia gota. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>7 </p></td> 
  <td class="- topic/stentry stentry"> <p>Suspensão do papel de parede. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>8 </p></td> 
  <td class="- topic/stentry stentry"> <p>Reverter o papel de parede travado. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>9 </p></td> 
  <td class="- topic/stentry stentry"> <p>Suspensão aleatória de papel de parede. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>10º </p></td> 
  <td class="- topic/stentry stentry"> <p>Queda aleatória. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>11º </p></td> 
  <td class="- topic/stentry stentry"> <p>Aleatório. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>12º </p></td> 
  <td class="- topic/stentry stentry"> <p>Metade da frente. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>13º </p></td> 
  <td class="- topic/stentry stentry"> <p>Espelho (correspondência de marcadores). </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>14. </p></td> 
  <td class="- topic/stentry stentry"> <p>Aleatório padrão. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>15. </p></td> 
  <td class="- topic/stentry stentry"> <p>Aleatório de alta frequência. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>16º </p></td> 
  <td class="- topic/stentry stentry"> <p>Aleatório de baixa frequência. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>17º </p></td> 
  <td class="- topic/stentry stentry"> <p>Aleatório horizontal. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>18º </p></td> 
  <td class="- topic/stentry stentry"> <p>Aleatório vertical. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>19º </p></td> 
  <td class="- topic/stentry stentry"> <p>Edge randomizer. </p></td> 
 </tr> 
</table>

## Padrão {#section-23fba3bd1f3544c7913d12f2ca148517}

0 (repetição direta).

## Consulte também {#section-a08887a91db34ed3b183899c69c9f74f}

[repetir=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8)
