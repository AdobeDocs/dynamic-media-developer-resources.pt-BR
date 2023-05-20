---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de clique duplo/toque para ações de rotação. Configuração para <span class="codeph"> nenhum </span> desativa a rotação de clique duplo/toque. Se definida como <span class="codeph"> zoom </span>, clicar na imagem gira em uma etapa de rotação; CTRL+Clique gira em uma etapa de rotação. Configuração para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina a rotação para o nível inicial. Para <span class="codeph"> zoomReset </span>, reset é aplicada se o fator de rotação atual estiver no limite especificado ou além dele, caso contrário, a rotação é aplicada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Padrão {#section-7a2128fd488941948aff18421f533ccf}

`reset` em computadores de secretária; `zoomReset` em dispositivos sensíveis ao toque.

## Exemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
