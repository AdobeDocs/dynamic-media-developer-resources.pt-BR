---
title: PageView.iconEffect
description: PageView.iconEffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: cdd96e58-d805-47d6-bf26-9ebd90afd535
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# PageView.iconEffect{#pageview-iconeffect}

` [PageView.|<containerId>_pageView.]iconeffect=0|1[, *`contagem`*][, *`esmaecer`*][, *`autoHide`*]`

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Habilita o iconeffect <span class="codeph"></span> para ser exibido na parte superior da imagem quando ela estiver em um estado de redefinição e sugerir uma ação disponível para interagir com a imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">contagem</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o número máximo de vezes que o <span class="codeph"> iconeffect</span> é exibido e reexibido. Um valor de <span class="codeph"> -1</span> indica que o ícone sempre reaparece indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração da animação de exibição ou ocultação, em segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Define o número de segundos durante os quais <span class="codeph"> iconeffect</span> permanece totalmente visível antes de ser ocultado automaticamente. Ou seja, o tempo após a conclusão da animação de fade-in, mas antes do início da animação de fade-out. Uma configuração de <span class="codeph"> 0</span> desabilita o comportamento de ocultação automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-b6e5e52698d4492f9d6350e7e312bb1b}

Opcional.

## Padrão {#section-7d0fc8fa09b34c288ed32ef7faa84604}

`1,1,0.3,3`

## Exemplo {#section-95db1bfcccf241089654363203b19977}

`iconeffect=0`
