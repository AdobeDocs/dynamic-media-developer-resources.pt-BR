---
title: SetIndicator.autohide
description: SetIndicator.autohide
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 75521239-a0be-4aa0-b65d-9a1f7d902cf2
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`limite`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> limite</span>]</span> </p> </td> 
   <td colname="col2"> <p> Configura o comportamento de ocultação automática dependendo do número de páginas e do tamanho dos componentes de tempo de execução. </p> <p> <span class="codeph"> 0</span> desativa a ocultação automática. </p> <p> <span class="codeph"> 1</span> habilita a ocultação automática. O componente oculta os pontos se pelo menos uma das condições a seguir for verdadeira: </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">a linha com pontos se torna mais larga que a largura do componente de tempo de execução, ou </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">o número de páginas definido para este componente excede o limite configurado pelo parâmetro <span class="codeph"><span class="varname"> limit</span></span>. </li> 
     </ul> </p> <p> A configuração de <span class="codeph"><span class="varname"> limite</span></span> a <span class="codeph"> -1</span> desabilita a segunda condição de ocultação automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`1,10`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
