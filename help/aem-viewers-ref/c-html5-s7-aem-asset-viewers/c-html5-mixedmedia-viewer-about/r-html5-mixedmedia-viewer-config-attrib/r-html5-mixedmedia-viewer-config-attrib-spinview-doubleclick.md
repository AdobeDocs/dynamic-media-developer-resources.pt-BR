---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de duplo clique/toque para girar ações. Configurar como <span class="codeph"> nenhum </span> desativa o duplo clique/toque em rotação. Se estiver definido como <span class="codeph"> zoom </span>, clicar na imagem gira em uma etapa de rotação; CTRL+Clique gira uma etapa de rotação. Configurar como <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o giro para o nível inicial de rotação. Para <span class="codeph"> zoomReset </span>, a redefinição será aplicada se o fator de rotação atual estiver dentro ou além do limite especificado, caso contrário, a rotação será aplicada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` Em computadores de mesa; `zoomReset` em dispositivos de toque.

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
