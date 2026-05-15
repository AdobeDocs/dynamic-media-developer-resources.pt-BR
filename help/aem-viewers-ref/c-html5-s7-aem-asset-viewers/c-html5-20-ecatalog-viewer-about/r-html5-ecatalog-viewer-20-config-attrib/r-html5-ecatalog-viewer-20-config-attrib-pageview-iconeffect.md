---
title: PageView.iconEffect
description: PageView.iconEffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: cdd96e58-d805-47d6-bf26-9ebd90afd535
TQID: 'https://experienceleague.adobe.com/BChSE62IgfhsabTf1I-XlAJLqvRhai4U48vNEg-MkQ4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 1%

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
