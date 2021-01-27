---
description: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
topic: Dynamic Media
uuid: 42327f03-269b-4d4e-a35d-2537ca3ba071
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---


# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoom|Reset  </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de ações de clique/toque único para aplicar zoom. A configuração para <span class="codeph"> none </span> desativa o zoom de clique único/toque. Se definido para <span class="codeph"> zoom </span> clicando no zoom da imagem em uma etapa de zoom; CTRL+Clique diminui o zoom em uma etapa. Definir para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o zoom para o nível de zoom inicial. Para <span class="codeph"> zoomReset </span>, a redefinição será aplicada se o fator de zoom atual estiver dentro ou acima do limite especificado, caso contrário o zoom será aplicado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-50bcd15223174bb79ce08b31ea03d682}

Opcional.

## Padrão {#section-7564169749ff4a4996049ea1148cb2a5}

`zoomReset` sobre computadores de secretária;  `none` em dispositivos de toque.

## Exemplo {#section-96e69b70365f461dae4399e49044ea2f}

`singleclick=zoom`
