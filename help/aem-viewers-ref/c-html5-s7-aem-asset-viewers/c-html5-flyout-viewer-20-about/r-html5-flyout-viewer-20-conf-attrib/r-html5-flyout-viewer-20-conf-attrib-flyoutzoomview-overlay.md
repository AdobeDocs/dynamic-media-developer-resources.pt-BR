---
description: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flyout
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 1%

---


# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Controla a aparência do realce da exibição principal quando o flyout está ativo. Quando definido como <span class="codeph"> 0</span>, a área atualmente visível na janela do flyout é realçada usando os estilos fornecidos pelo <span class="codeph"> .s7highlight</span> ou <span class="codeph"> .s7cursor</span> nomes de classe CSS (dependendo do valor do <span class="codeph"> modificador do modo de realce</span>). Quando definido como <span class="codeph"> 1</span> componente entra no modo "inverso", onde a área visualizada atualmente é totalmente transparente (no caso de <span class="codeph"> realce mode</span> estar definido como <span class="codeph"> realce</span>) ou estilizado com <span class="codeph"> .s7cursor</span> CSS nome da classe (no caso <span class="codeph"> realce mode</span> está definido como <span class="codeph"> cursor</span>), mas a área ao redor é preenchida usando estilos fornecidos pelo <span class="codeph"> .s7overlay</span> nome da classe CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Exemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
