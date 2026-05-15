---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: faec00b3-b981-4831-bc97-dff442389133
TQID: 'https://experienceleague.adobe.com/pVlxftuVZ3kgRfQElIXwGcoTgjWduRisjcBZGKq85LE'
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

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`contagem`*][, *`esmaecer`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Permite que o IconEffect seja exibido na parte superior da imagem quando ela estiver em um estado de redefinição e sugere uma ação disponível para interagir com a imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contagem</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica o número máximo de vezes que o IconEffect aparece e reaparece. Um valor de <span class="codeph"> -1</span> indica que o ícone sempre reaparece indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fade</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração da animação de exibição ou ocultação, em segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p>Define o número de segundos que o IconEffect permanece totalmente visível antes de ser ocultado automaticamente. Ou seja, o tempo após a conclusão da animação de fade-in, mas antes do início da animação de fade-out. Uma configuração de <span class="codeph"> 0</span> desabilita o comportamento de ocultação automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-50bcd15223174bb79ce08b31ea03d682}

Opcional.

## Padrão {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1,0.3,3`

## Exemplo {#section-96e69b70365f461dae4399e49044ea2f}

`iconeffect=0`
