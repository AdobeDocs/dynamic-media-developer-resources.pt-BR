---
description: nulo
seo-description: nulo
seo-title: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
topic: Dynamic media
uuid: e6e9e97c-5d9b-47ca-bae3-ed3371c5ff9b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Controla a aparência do realce da visualização principal quando o flyout está ativo. Quando definida como <span class="codeph"> 0</span>, a área atualmente visível na janela do flyout é realçada usando os estilos fornecidos pelos nomes das classes <span class="codeph"> .s7destacar</span> ou <span class="codeph"> .s7cursor</span> CSS (dependendo do valor do modificador do modo de <span class="codeph"> realce</span> ). Quando definido como <span class="codeph"> 1</span> componente entra no modo "inverso", onde a área visualizada atualmente é totalmente transparente (no caso de o modo <span class="codeph"> de realce estar definido como</span> realce <span class="codeph"> ) ou estilizada com o nome da classe</span>.s7cursor <span class="codeph"> CSS (no caso de o modo</span> de realce estar definido como o cursor de sobreposição), mas a área circundante é preenchida usando estilos fornecidos pelo nome da classe .s7over <span class="codeph"></span> <span class="codeph"></span><span class="codeph"></span> CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Example {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
