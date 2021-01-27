---
description: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
topic: Dynamic Media
uuid: e6e9e97c-5d9b-47ca-bae3-ed3371c5ff9b
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Controla a aparência do realce da visualização principal quando o flyout está ativo. Quando definida como <span class="codeph"> 0</span>, a área atualmente visível na janela do flyout é realçada usando os estilos fornecidos pelo <span class="codeph"> .s7destacar</span> ou <span class="codeph"> .s7cursor</span> nomes de classe CSS (dependendo do valor do modificador <span class="codeph"> Highlight mode</span>). Quando definido como <span class="codeph"> 1</span> o componente entra no modo "inverso", onde a área visualizada atualmente é totalmente transparente (caso <span class="codeph"> modo de realce</span> esteja definido como <span class="codeph"> realce</span>) ou tenha o estilo <span class="codeph"> .s7cursor</span> nome da classe CSS (no caso <span class="codeph"> modo de realce&lt;a&gt; está definida como <span class="codeph"> cursor</span>), mas a área circundante é preenchida usando estilos fornecidos pelo <span class="codeph"> .s7overlay</span> nome da classe CSS.</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Exemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
