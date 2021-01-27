---
description: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick
topic: Dynamic Media
uuid: b360db52-f705-4966-b77b-009bed729c25
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---


# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoom|Reset  </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de ações de clique/toque único para aplicar zoom. A configuração para <span class="codeph"> none </span> desativa o zoom de clique único/toque. Se definido para <span class="codeph"> girar </span> clicando no zoom da imagem em uma etapa de zoom; CTRL+Clique diminui o zoom em uma etapa. Configurar para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o zoom para o nível de rotação inicial. Para <span class="codeph"> zoomReset </span>, a redefinição será aplicada se o fator de zoom atual estiver dentro ou acima do limite especificado, caso contrário o zoom será aplicado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Padrão {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` sobre computadores de secretária;  `none` em dispositivos de toque.

## Exemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
