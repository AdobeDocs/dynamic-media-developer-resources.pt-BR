---
description: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
topic: Dynamic Media
uuid: 9539ede1-08fb-4bfc-8a5a-870c7d84de7f
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 1%

---


# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *``*[, *`duração`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|esmaecer|slide  </span> </p> </td> 
   <td colname="col2"> <p>Especifica o tipo de efeito aplicado na alteração de quadro. <span class="codeph"> nenhum  </span> significa nenhuma transição; mudança de quadro acontece instantaneamente. </p> <p> <span class="codeph"> desaparecimento gradual  </span> significa transição de desaparecimento gradual entre quadros antigos e novos. </p> <p> <span class="codeph"> o slide  </span> ativa a transição onde o quadro antigo desliza para fora da visualização e o novo quadro desliza para dentro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duração  </span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração (em segundo) do efeito de transição <span class="codeph"> fade </span> ou <span class="codeph"> slide </span>. </p> </td> 
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
