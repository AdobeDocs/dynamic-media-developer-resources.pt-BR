---
description: nulo
seo-description: nulo
seo-title: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
topic: Dynamic media
uuid: 9eab6cb2-92a3-41d2-999a-254a7109d6b6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Permite que o efeito <span class="codeph"> de</span> ícone seja exibido na parte superior da imagem quando ela está em um estado de redefinição e sugere uma ação disponível para interagir com a imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o número máximo de vezes que o <span class="codeph"> efeito</span> de ícone aparece e reaparece. Um valor de <span class="codeph"> -1</span> indica que o ícone sempre aparece indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> desvanecer</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração da animação de mostrar ou ocultar, em segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Define o número de segundos em que o <span class="codeph"> efeito</span> do ícone permanece totalmente visível antes de se ocultar automaticamente. Ou seja, o tempo após a animação de desaparecimento gradual é concluída, mas antes dos start de animação de desaparecimento gradual. Uma configuração de <span class="codeph"> 0</span> desativa o comportamento de ocultação automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
