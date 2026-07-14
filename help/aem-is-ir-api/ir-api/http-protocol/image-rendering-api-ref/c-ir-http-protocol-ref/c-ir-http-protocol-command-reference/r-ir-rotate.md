---
title: girar
description: Ângulo de rotação do material. Define o ângulo de rotação dos materiais.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
TQID: 'https://experienceleague.adobe.com/prSGGMuV4SpFfhd8uCVzMRGpr-VBpowxE-UagKtpnqI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# girar{#rotate}

Ângulo de rotação do material. Define o ângulo de rotação dos materiais.

` rotate= *`ângulo`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> ângulo </span> </p> </td> 
  <td class="stentry"> <p>Ângulo de rotação em graus (real). </p> </td> 
 </tr> 
</table>

Gire materiais de textura repetíveis (excluindo papéis de parede) em múltiplos de 45° quando aplicados a objetos planos ou objetos planos.

Girar materiais de textura repetíveis por ângulos arbitrários quando aplicados a Flowline e Sketch Objects.

Girar materiais decalques por ângulos arbitrários.

Os ângulos positivos giram no sentido horário. A textura ou o decalque é girado em torno do ponto âncora ( `anchor=`); o ponto âncora permanece alinhado com a origem do objeto de destino.

## Propriedades {#section-ad4d07897ca24f63af1a4062f8618e36}

Atributo de material. Ignorado por cor sólida, papel de parede, gabinete e materiais de tratamento de janela. *`angle`* Deve ser um múltiplo de 45 para texturas repetíveis, a menos que aplicado a Flowline ou Sketch Objects.

## Padrão {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, sem rotação.

## Consulte também {#section-f73c00e9368b478dac1fd15bb4367a12}

[anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)

