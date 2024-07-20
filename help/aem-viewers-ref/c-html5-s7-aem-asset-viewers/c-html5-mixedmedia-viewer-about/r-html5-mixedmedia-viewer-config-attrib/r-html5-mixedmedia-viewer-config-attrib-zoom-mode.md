---
title: zoomMode
description: Define o tipo de interação de zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---

# zoomMode{#zoommode}

Define o tipo de interação de zoom.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contínuo|em linha|automático </span> </p> </td> 
   <td colname="col2"> <p> O <span class="codeph"> continuous </span> habilita o zoom clássico no qual a imagem gradualmente dá zoom à medida que você clica, dá um toque duplo ou aperta na exibição principal. Para voltar à exibição inicial, reduza ou redefina o estado de zoom. A classe </p> <p> O <span class="codeph"> incorporado </span> habilita o zoom instantâneo, no qual a imagem com zoom é exibida instantaneamente à medida que você passa o mouse sobre a exibição principal no desktop ou para tocar e segurar um dispositivo de toque. A imagem reverte automaticamente para o estado inicial depois de mover o mouse da visualização ou soltar o dedo. No modo <span class="codeph"> embutido </span>, os conjuntos de imagens aninhados são nivelados e exibidos como miniaturas individuais. A classe <span class="codeph"> auto </span> ativa o modo embutido na área de trabalho e o modo contínuo em dispositivos de toque. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
