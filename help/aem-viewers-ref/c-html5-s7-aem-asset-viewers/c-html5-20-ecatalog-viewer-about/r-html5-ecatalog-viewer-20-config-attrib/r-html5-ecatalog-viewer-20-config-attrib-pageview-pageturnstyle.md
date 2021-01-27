---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
topic: Dynamic Media
uuid: 3192d810-fb30-44ae-9939-98e890c76e5c
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# PageView.pageturnstyle{#pageview-pageturnstyle}

` [PageView.|<containerId>_pageView.]pageturnstyle= *``*, *``*, *``*, *``*, *``*, *`diviserWidthdividerColordivOpacityborderOnOffborderColorfillColor`*`

Controla a aparência do componente quando um `PageView.frametransition` está definido para `turn` ou para `auto` em sistemas de desktop.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> divWidth</span></span> </p> </td> 
   <td colname="col2"> <p> A largura, em pixels, da sombra do divisor de página que separa as páginas esquerda e direita na página espelhada. Ele também controla a largura da sombra em execução exibida ao lado da página de viragem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> divOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> A cor da sombra no formato RRGGBB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> divOpacity</span></span> </p> </td> 
   <td colname="col2"> <p>A opacidade de sombra no intervalo de <span class="codeph"> 0</span> a <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> O sinalizador (<span class="codeph"> 0</span> ou <span class="codeph"> 1</span>) que ativa e desativa a borda em torno da página de viragem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> A cor da borda no formato RRGGBB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> A cor do preenchimento sólido da área do componente usada durante a animação de virada da página, no formato RRGGBB. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-54c634116cfe4f17813318e07539264c}

Opcional.

## Padrão {#section-43fd13f639c2480c82658fafeeaf0846}

`40,909090,1,1,909090,FFFFFF`

## Exemplos {#section-bb97b2aac37a43eba11d263ce7049363}

`pageturnstyle=20,FF0000,1,1,00FF00,0000FF`
