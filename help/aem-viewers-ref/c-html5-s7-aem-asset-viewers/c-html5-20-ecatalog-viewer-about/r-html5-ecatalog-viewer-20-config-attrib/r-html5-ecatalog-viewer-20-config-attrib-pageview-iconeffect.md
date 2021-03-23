---
description: PageView.iconEffect
solution: Experience Manager
title: PageView.iconEffect
uuid: c8adabf9-ccbf-4a46-b1e7-b4cb58d4e606
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 1%

---


# PageView.iconEffect{#pageview-iconeffect}

` [PageView.|<containerId>_pageView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
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

## Propriedades {#section-b6e5e52698d4492f9d6350e7e312bb1b}

Opcional.

## Padrão {#section-7d0fc8fa09b34c288ed32ef7faa84604}

`1,1,0.3,3`

## Exemplo {#section-95db1bfcccf241089654363203b19977}

`iconeffect=0`
