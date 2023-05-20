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
ht-degree: 0%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de clique duplo/toque para ações de rotação. Configuração para <span class="codeph"> nenhum </span> desativa a rotação de clique duplo/toque. Se definida como <span class="codeph"> zoom </span>, clicar na imagem gira em uma etapa de rotação; CTRL+Clique gira em uma etapa de rotação. Configuração para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina a rotação para o nível inicial. Para <span class="codeph"> zoomReset </span>, reset é aplicada se o fator de rotação atual estiver no limite especificado ou além dele, caso contrário, a rotação é aplicada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` Em computadores de secretária; `zoomReset` em dispositivos sensíveis ao toque.

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
