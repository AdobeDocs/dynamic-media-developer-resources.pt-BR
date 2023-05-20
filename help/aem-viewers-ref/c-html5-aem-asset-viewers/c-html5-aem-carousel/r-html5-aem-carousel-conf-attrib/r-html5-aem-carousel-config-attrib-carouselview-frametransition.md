---
title: CarouselView.frametransition
description: CarouselView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`duração`*[, *`espaçamento`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|esmaecer|slide </span> </p> </td> 
   <td colname="col2"> <p>Especifica o tipo do efeito aplicado na alteração do quadro. Por exemplo, <span class="codeph"> nenhum </span> significa sem transição; a alteração de quadro ocorre instantaneamente. E, </p> <p> <span class="codeph"> fade </span> significa transição cross-fade entre quadros antigos e novos. Por último, </p> <p> <span class="codeph"> slide </span> ativa a transição em que o quadro antigo desaparece da exibição e o novo quadro surge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duração </span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração (em segundos) de <span class="codeph"> fade </span> ou <span class="codeph"> slide </span> efeito de transição. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> espaçamento </span> </span> </p> </td> 
   <td colname="col2"> <p>O espaçamento entre os quadros adjacentes em <span class="codeph"> slide </span> transição, tem o intervalo de <span class="codeph"> 0 </span> até <span class="codeph"> 1 </span> e é relativo à largura do componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

Nenhum.

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
