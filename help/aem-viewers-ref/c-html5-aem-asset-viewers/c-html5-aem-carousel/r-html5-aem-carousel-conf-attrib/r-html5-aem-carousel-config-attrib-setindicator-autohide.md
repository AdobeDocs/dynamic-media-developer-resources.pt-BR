---
description: SetIndicator.autohide
solution: Experience Manager
title: SetIndicator.autohide
uuid: eb93ad7a-6176-47ed-92c6-2eb1afcac0eb
feature: Dynamic Media Classic,Visualizadores,SDK/API,Banners em carrossel
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 1%

---


# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`limite`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[, <span class="varname"> limite</span>]</span> </p> </td> 
   <td colname="col2"> <p> Configura o comportamento de ocultação automática, dependendo do número de páginas e do tamanho do componente de tempo de execução. </p> <p> <span class="codeph"> 0</span> desativa a ocultação automática. </p> <p> <span class="codeph"> 1</span> ativa a ocultação automática. O componente oculta seus pontos se pelo menos uma das seguintes condições se tornar verdadeira: </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">a linha com pontos se torna maior que a largura do componente de tempo de execução, ou </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">o número de páginas definidas para este componente excede o limite configurado pelo parâmetro <span class="codeph"><span class="varname"> limit</span></span>. </li> 
     </ul> </p> <p> Definir <span class="codeph"><span class="varname"> limite</span></span> para <span class="codeph"> -1</span> desativa a segunda condição de ocultação automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`1,10`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
