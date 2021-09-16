---
title: CarouselView.frametransition
description: CarouselView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *``*[, *`espaçamento entre durações`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|esmaecer|slide  </span> </p> </td> 
   <td colname="col2"> <p>Especifica o tipo de efeito aplicado na alteração de quadro. Por exemplo, <span class="codeph"> nenhum </span> representa nenhuma transição; a mudança de quadro ocorre instantaneamente. E, </p> <p> <span class="codeph"> desvanecer  </span> significa uma transição entre o desvanecimento dos quadros antigos e novos. Por último, </p> <p> <span class="codeph"> o slide  </span> ativa a transição, onde o quadro antigo desliza para fora da exibição e os novos slides do quadro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration  </span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração (em segundo) do <span class="codeph"> desvanecimento </span> ou <span class="codeph"> slide </span> efeito de transição. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> espaçamento  </span> </span> </p> </td> 
   <td colname="col2"> <p>O espaçamento entre quadros adjacentes na transição <span class="codeph"> slide </span> tem o intervalo de <span class="codeph"> 0 </span> a <span class="codeph"> 1 </span> e é relativo à largura do componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

Nenhum.

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
