---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de rotação
role: Developer,Business Practitioner
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 1%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de duplo clique/toque para girar ações. Configurar para <span class="codeph"> nenhum </span> desativa o duplo clique/toque em rotação. Se definido como <span class="codeph"> zoom </span>, clicar na imagem gira em uma etapa de rotação; CTRL+Clique gira uma etapa de rotação. Configurar para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o giro para o nível inicial de rotação. Para <span class="codeph"> zoomReset </span>, a redefinição é aplicada se o fator de rotação atual estiver no limite especificado ou além dele, caso contrário a rotação é aplicada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Padrão {#section-7a2128fd488941948aff18421f533ccf}

`reset` em computadores de secretária;  `zoomReset` em dispositivos de toque.

## Exemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
