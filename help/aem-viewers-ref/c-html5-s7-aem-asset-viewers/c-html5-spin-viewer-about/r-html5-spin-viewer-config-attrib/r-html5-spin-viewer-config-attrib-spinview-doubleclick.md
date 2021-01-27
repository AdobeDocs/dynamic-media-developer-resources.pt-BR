---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
topic: Dynamic Media
uuid: c1eef3d1-471e-41ef-b899-008d45b616d0
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoom|Reset  </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de duplo-clique/toque para girar ações. A configuração para <span class="codeph"> none </span> desativa a rotação do duplo-clique/toque. Se definido como <span class="codeph"> zoom </span> clicando na imagem gira em uma etapa de rotação; CTRL+Clique gira uma etapa de rotação para fora. Configurar para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina a rotação para o nível de rotação inicial. Para <span class="codeph"> zoomReset </span>, a redefinição será aplicada se o fator de rotação atual estiver dentro ou acima do limite especificado, caso contrário a rotação será aplicada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Padrão {#section-7a2128fd488941948aff18421f533ccf}

`reset` sobre computadores de secretária;  `zoomReset` em dispositivos de toque.

## Exemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
