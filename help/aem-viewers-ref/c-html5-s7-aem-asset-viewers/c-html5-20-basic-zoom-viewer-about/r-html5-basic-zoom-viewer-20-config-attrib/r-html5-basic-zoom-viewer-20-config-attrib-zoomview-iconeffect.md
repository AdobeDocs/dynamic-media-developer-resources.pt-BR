---
description: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
uuid: 38350e3d-515b-454c-bc85-39b91ad06e8b
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 1%

---


# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Permite que o IconEffect seja exibido na parte superior da imagem quando ela está em um estado de redefinição e é sugestivo de uma ação disponível para interagir com a imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica o número máximo de vezes em que o IconEffect é exibido e reaparece. Um valor de <span class="codeph"> -1</span> indica que o ícone sempre aparece indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> desaparecer</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração da animação show ou hide, em segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p>Define o número de segundos em que o IconEffect permanece totalmente visível antes de se ocultar automaticamente. Ou seja, o tempo depois que a animação de esmaecimento é concluída, mas antes do início da animação de esmaecimento. Uma configuração de <span class="codeph"> 0</span> desativa o comportamento de ocultação automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-50bcd15223174bb79ce08b31ea03d682}

Opcional.

## Padrão {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1,0.3,3`

## Exemplo {#section-96e69b70365f461dae4399e49044ea2f}

`iconeffect=0`
