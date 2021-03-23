---
description: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode
uuid: 397c1af0-f806-4555-83fa-ec7548b59a60
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flyout
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> destaque|cursor  </span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de quadro de navegação a ser usado. Quando definido como <span class="codeph"> cursor </span>, o componente usa um cursor de referência de tamanho fixo. É possível ter uma arte de cursor diferente para sistemas de desktop e dispositivos de toque, isso é controlado com <span class="codeph"> .s7cursor </span> classe CSS e <span class="codeph"> input=mouse|touch </span> seletor de atributo. Em sistemas de desktop, um ponto de ancoragem é definido no meio da área do cursor, enquanto em dispositivos de toque a âncora está localizada no centro inferior do cursor. Quando definido para <span class="codeph"> realçar </span>, o componente usa um quadro de navegação de tamanho variável; o tamanho e a forma do quadro dependem do fator de zoom e do tamanho da exibição do flyout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> Define o tempo (em segundos) necessário para o realce ou o cursor se esmaecerem depois de serem ativados pelo usuário. A introdução gradual só é aplicada aos dispositivos de toque; em sistemas de desktop, ele é ignorado pelo componente. </p> <p>O Fade in se aplica aos seguintes elementos da interface do usuário: quadro de realce, cursor fixo, sobreposição (caso o parâmetro <span class="codeph"> sobreposição </span> esteja definido como <span class="codeph"> 1 </span>). A animação de exibição de layout começa somente após a conclusão do realce/cursor em animação. Não há animação esmaecida. Quando o usuário desativa o menu , os elementos da interface do usuário correspondentes (cursor, realce e sobreposição) são ocultados instantaneamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free  </span> </p> </td> 
   <td colname="col2"> <p> Controla o posicionamento do quadro de navegação. </p> <p>Se definido como <span class="codeph"> na imagem </span> o quadro de navegação só poderá ser posicionado dentro da área da imagem real dentro da exibição principal. </p> <p>Se definido como <span class="codeph"> livre </span>, um usuário pode mover o quadro de navegação em qualquer lugar na área de visualização principal lógica, mesmo fora do conteúdo da imagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Exemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
