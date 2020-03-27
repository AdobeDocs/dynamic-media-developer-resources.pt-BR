---
description: nulo
seo-description: nulo
seo-title: CarouselView.enableHD
solution: Experience Manager
title: CarouselView.enableHD
topic: Dynamic media
uuid: 17df4a68-a251-427c-a3c4-1e0679e3f8f1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`número`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sempre|nunca|limite</span> </p> </td> 
   <td colname="col2"> <p> Ative, limite ou desative a otimização para dispositivos em que <span class="codeph"> devicePixelRatio</span> é maior que <span class="codeph"> 1</span>, ou seja, dispositivos com tela de alta densidade como iPhone4 e dispositivos semelhantes. </p> <p>Se ativo, o componente limita o tamanho da solicitação de imagem IS como se o dispositivo tivesse apenas uma proporção de pixel de <span class="codeph"> 1</span> e, dessa forma, reduzindo a largura de banda. </p> <p>Consulte o exemplo abaixo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> número</span></span> </p> </td> 
   <td colname="col2"> <p> Se estiver usando a configuração de <span class="codeph"> limite</span> , o componente ativará a alta densidade de pixels apenas até o limite especificado. </p> <p>Consulte o exemplo abaixo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
