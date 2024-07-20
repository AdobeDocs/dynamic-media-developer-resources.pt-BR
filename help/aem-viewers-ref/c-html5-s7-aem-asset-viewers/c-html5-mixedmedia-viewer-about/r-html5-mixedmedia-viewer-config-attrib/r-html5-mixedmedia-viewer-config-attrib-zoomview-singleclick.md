---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0fcc1f5c-a735-430d-be0c-c00ed08830df
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de clique único/toque para ações de zoom. Configurar como <span class="codeph"> nenhum </span> desabilita o zoom de clique único/toque. Se estiver definido como <span class="codeph">, o zoom </span> ao clicar na imagem dá zoom de uma só vez; CTRL+Clique dá zoom de uma só vez. Configurar como <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o zoom para o nível inicial. Para <span class="codeph"> zoomReset </span>, a redefinição é aplicada se o fator de zoom atual estiver no limite especificado ou além dele, caso contrário o zoom é aplicado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` em computadores desktop; `none` em dispositivos de toque.

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
