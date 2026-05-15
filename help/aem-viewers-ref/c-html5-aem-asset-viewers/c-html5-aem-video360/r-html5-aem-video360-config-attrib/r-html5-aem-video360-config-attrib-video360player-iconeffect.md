---
title: Video360Player.iconeffect
description: Atributo de configuração para o Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 818ea14b-4dab-4447-9645-46f2ba82547b
TQID: 'https://experienceleague.adobe.com/hi-8zIddM3Pybmh38PWiMSYuSY5COz9FnJpZs3FJ6yE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 1%

---

# Video360Player.iconeffect{#video-player-iconeffect}

Atributo de configuração para o Video360 Viewer.

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *`contagem`*][, *`esmaecer`*][, *`autoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Permite que o IconEffect seja exibido na parte superior do vídeo quando ele estiver no estado pausado. Em alguns dispositivos, os controles nativos são usados. Nesses casos, o modificador <span class="codeph">iconeffect</span> será ignorado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">contagem</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o número máximo de vezes que o IconEffect aparece e reaparece. Um valor de <span class="codeph"> -1</span> indica que o ícone reaparece indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica a duração da animação de exibição ou ocultação, em segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Define o número de segundos que o IconEffect permanece totalmente visível antes de ser ocultado automaticamente. Ou seja, o tempo depois que a animação de desaparecimento gradual é concluída e antes que a animação de desaparecimento gradual seja iniciada. Defina como <span class="codeph"> 0</span> para desabilitar o comportamento de ocultação automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
