---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Controla a aparência do destaque da exibição principal quando a imagem suspensa está ativa. Quando definido como <span class="codeph"> 0</span>, a área visível na janela da imagem suspensa é realçada com os estilos fornecidos pelo <span class="codeph"> .s7highlight</span> ou por <span class="codeph"> .s7cursor</span> Nomes de classe CSS (dependendo do valor de <span class="codeph"> modo realce</span> modificador). Quando definido como <span class="codeph"> 1</span> entra no modo "inverso" onde a área visualizada atualmente é totalmente transparente (caso <span class="codeph"> modo realce</span> está definida como <span class="codeph"> realçar</span>) ou estilizado com <span class="codeph"> .s7cursor</span> Nome da classe CSS (caso esteja <span class="codeph"> modo realce</span> está definida como <span class="codeph"> cursor</span>), mas a área ao redor é preenchida com estilos fornecidos por <span class="codeph"> .s7overlay</span> Nome da classe CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Exemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
