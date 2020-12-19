---
description: nulo
seo-description: nulo
seo-title: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode
topic: Dynamic media
uuid: 397c1af0-f806-4555-83fa-ec7548b59a60
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> destaque|cursor  </span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de quadro de navegação a ser usado. Quando definido como <span class="codeph"> cursor </span>, o componente usa um cursor de referência de tamanho fixo. É possível ter uma arte de cursor diferente para sistemas de desktop e dispositivos de toque, isso é controlado com o seletor de atributos <span class="codeph"> .s7cursor </span> CSS e <span class="codeph"> input=mouse|touch </span>. Nos sistemas desktop, um ponto de ancoragem é definido no meio da área do cursor, enquanto nos dispositivos de toque a âncora está localizada no centro inferior do cursor. Quando definido para <span class="codeph"> realçar </span>, o componente usa um quadro de navegação de tamanho variável; o tamanho e a forma do quadro dependem do fator de zoom e do tamanho da visualização do flyout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> Define o tempo (em segundos) que leva o realce ou o cursor a desaparecer depois de ser ativado pelo usuário. O aparecimento gradual é aplicado apenas em dispositivos de toque; em sistemas de desktop, ele é ignorado pelo componente. </p> <p>O Fade in se aplica aos seguintes elementos da interface do usuário: quadro de destaque, cursor fixo, sobreposição (caso o parâmetro <span class="codeph"> overlay </span> esteja definido como <span class="codeph"> 1 </span>). A animação de visualização de menu suspenso só começa depois que o realce/cursor desaparece na animação é concluída. Não há animação de desaparecer. Quando o usuário desativa o flyout, os elementos de interface correspondentes (cursor, realce e sobreposição) são ocultados instantaneamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free  </span> </p> </td> 
   <td colname="col2"> <p> Controla o posicionamento do quadro de navegação. </p> <p>Se definido como <span class="codeph"> onimage </span>, o quadro de navegação só pode ser posicionado dentro da área da imagem real dentro da visualização principal. </p> <p>Se definido como <span class="codeph"> free </span>, um usuário pode mover o quadro de navegação para qualquer lugar na área de visualização principal lógica, mesmo fora do conteúdo da imagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Exemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
