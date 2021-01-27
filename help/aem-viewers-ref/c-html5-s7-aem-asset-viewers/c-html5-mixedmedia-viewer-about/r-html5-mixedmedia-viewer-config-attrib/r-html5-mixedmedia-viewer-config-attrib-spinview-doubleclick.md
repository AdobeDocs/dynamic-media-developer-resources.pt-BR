---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
topic: Dynamic Media
uuid: 8e78d91e-e4c6-40f1-9421-8da8bc404ee0
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoom|Reset  </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de duplo-clique/toque para girar ações. A configuração para <span class="codeph"> none </span> desativa a rotação do duplo-clique/toque. Se definido como <span class="codeph"> zoom </span> clicando na imagem gira em uma etapa de rotação; CTRL+Clique gira uma etapa de rotação para fora. Configurar para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina a rotação para o nível de rotação inicial. Para <span class="codeph"> zoomReset </span>, a redefinição será aplicada se o fator de rotação atual estiver dentro ou acima do limite especificado, caso contrário a rotação será aplicada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` sobre computadores de secretária;  `zoomReset` em dispositivos de toque.

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
