---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 9f52542e-398c-45a2-89ea-95c9aefbde3e
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de duplo clique/toque para aplicar zoom às ações. Configurar como <span class="codeph"> nenhum </span> desativa o zoom de duplo clique/toque. Se estiver definido como <span class="codeph"> zoom </span> clicar nos zoom da imagem em uma etapa de zoom; CTRL + Clique com o zoom para baixo em uma etapa de zoom. Configurar como <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o zoom para o nível de zoom inicial. Para <span class="codeph"> zoomReset </span>, a redefinição será aplicada se o fator de zoom atual estiver acima ou acima do limite especificado, caso contrário, o zoom será aplicado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`reset` - Em computadores de secretária; `zoomReset` em dispositivos de toque.

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`doubleclick=zoom`
