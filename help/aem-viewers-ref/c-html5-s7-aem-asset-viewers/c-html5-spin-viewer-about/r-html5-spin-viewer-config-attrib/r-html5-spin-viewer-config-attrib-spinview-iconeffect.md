---
description: SpinView.iconeffect
solution: Experience Manager
title: SpinView.iconeffect
uuid: 864fb8dc-34f8-4216-b38c-cc00f7d8d95f
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de rotação
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---


# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Permite que o ícone <span class="codeph"></span> seja exibido na parte superior da imagem quando ela está em um estado de redefinição e é sugestivo de uma ação disponível para interagir com a imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o número máximo de vezes em que o ícone <span class="codeph"></span> aparece e reaparece. Um valor de <span class="codeph"> -1</span> indica que o ícone sempre aparece indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> desaparecer</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração da animação show ou hide, em segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Define o número de segundos em que o ícone <span class="codeph"></span> permanece totalmente visível antes de se ocultar automaticamente. Ou seja, o tempo depois que a animação de esmaecimento é concluída, mas antes do início da animação de esmaecimento. Uma configuração de <span class="codeph"> 0</span> desativa o comportamento de ocultação automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Padrão {#section-7a2128fd488941948aff18421f533ccf}

`1,1,0.3,3`

## Exemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`iconeffect=0`
