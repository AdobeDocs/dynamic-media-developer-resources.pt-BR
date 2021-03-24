---
description: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
feature: Dynamic Media Classic,Visualizadores,SDK/API,Banners em carrossel
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *``*[, *`espaçamento entre durações`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|esmaecer|slide  </span> </p> </td> 
   <td colname="col2"> <p>Especifica o tipo de efeito aplicado na alteração de quadro. <span class="codeph"> nenhum  </span> significa transição; a mudança de quadro ocorre instantaneamente. </p> <p> <span class="codeph"> desvanecer  </span> significa uma transição entre o desvanecimento dos quadros antigos e novos. </p> <p> <span class="codeph"> o slide  </span> ativa a transição, onde o quadro antigo desliza para fora da exibição e os novos slides do quadro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration  </span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração (em segundo) do <span class="codeph"> desvanecimento </span> ou <span class="codeph"> slide </span> efeito de transição. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> espaçamento  </span> </span> </p> </td> 
   <td colname="col2"> <p>O espaçamento entre quadros adjacentes na transição <span class="codeph"> slide </span> tem o intervalo entre <span class="codeph"> 0 </span> e <span class="codeph"> 1 </span> e é relativo à largura do componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

Nenhum.

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
