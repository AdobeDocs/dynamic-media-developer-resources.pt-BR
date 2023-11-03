---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> destacar|cursor </span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de quadro de navegação a ser usado. Quando definido como <span class="codeph"> cursor </span>, o componente usa um cursor de referência de tamanho fixo. É possível ter diferentes artes de cursor para sistemas de desktop e dispositivos de toque. Essa capacidade é controlada com <span class="codeph"> .s7cursor </span> Classe CSS e <span class="codeph"> input=mouse|touch </span> seletor de atributo. Em sistemas desktop, um ponto de ancoragem é definido no meio da área de cursor, enquanto em dispositivos de toque a âncora está no centro inferior do cursor. Quando definido como <span class="codeph"> realçar </span>, o componente usa um quadro de navegação de tamanho variável; o tamanho e a forma do quadro dependem do fator de zoom e do tamanho da exibição da imagem suspensa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> Define o tempo (em segundos) necessário para que o destaque ou cursor apareça gradualmente após ser ativado pelo usuário. O fade in é aplicado apenas em dispositivos de toque; em sistemas de desktop, é ignorado pelo componente. </p> <p>O desaparecimento gradual se aplica aos seguintes elementos da interface do usuário: quadro de realce, cursor fixo, sobreposição (caso <span class="codeph"> sobreposição </span> está definido como <span class="codeph"> 1 </span>). A animação da exibição de imagem suspensa começa somente após a conclusão do destaque/cursor. Não há animação de desaparecimento gradual. Quando o usuário desativa a imagem suspensa, os elementos da interface do usuário correspondentes (cursor, destaque e sobreposição) são ocultados instantaneamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> Controla o posicionamento do quadro de navegação. </p> <p>Se definida como <span class="codeph"> onimage </span>, o quadro de navegação só pode ser posicionado dentro da área de imagem real na exibição principal. </p> <p>Se definida como <span class="codeph"> grátis </span> um usuário pode mover o quadro de navegação para qualquer lugar na área de exibição principal lógica, mesmo fora do conteúdo da imagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Exemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
