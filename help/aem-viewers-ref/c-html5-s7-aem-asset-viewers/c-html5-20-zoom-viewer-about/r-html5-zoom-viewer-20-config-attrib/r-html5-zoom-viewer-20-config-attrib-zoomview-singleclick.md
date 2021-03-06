---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3fd5b907-faf6-4d36-8ee1-79f3ace781d4
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de ações de clique/toque único para aumentar o zoom. Configurar como <span class="codeph"> nenhum </span> desativa o zoom de clique/toque único. Se estiver definido como <span class="codeph"> zoom </span> clicar nos zoom da imagem em uma etapa de zoom; CTRL + Clique com o zoom para baixo em uma etapa de zoom. Configurar como <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o zoom para o nível de zoom inicial. Para <span class="codeph"> zoomReset </span>, a redefinição será aplicada se o fator de zoom atual estiver acima ou acima do limite especificado, caso contrário, o zoom será aplicado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`zoomReset` - Em computadores de secretária; `none` em dispositivos de toque.

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
