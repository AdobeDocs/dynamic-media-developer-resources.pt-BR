---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 92a497dc-c6b5-4b2d-8095-08bc6ad3d189
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de clique único/toque para ações de zoom. Configuração para <span class="codeph"> nenhum </span> desativa o zoom de clique único/toque. Se definida como <span class="codeph"> rotação </span> clicar na imagem dá zoom em uma etapa de zoom; CTRL+Clique dá zoom em uma etapa de zoom. Configuração para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o zoom para o nível de rotação inicial. Para <span class="codeph"> zoomReset </span>, reset será aplicada se o fator de zoom atual estiver no limite especificado ou ultrapassá-lo, caso contrário, o zoom será aplicado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Padrão {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` Em computadores de secretária; `none` em dispositivos sensíveis ao toque.

## Exemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
