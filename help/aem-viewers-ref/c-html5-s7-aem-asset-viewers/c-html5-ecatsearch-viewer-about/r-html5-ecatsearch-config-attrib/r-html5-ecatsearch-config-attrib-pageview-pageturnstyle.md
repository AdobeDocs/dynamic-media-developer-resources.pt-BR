---
description: nulo
seo-description: nulo
seo-title: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
topic: Dynamic media
uuid: 748adb73-bfb6-4fce-aa6a-4216184edabb
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *``*, *``*, *``*, *``*, *``*, *`diviserWidthdividerColordivOpacityborderOnOffborderColorfillColor`*`]

Controla a aparência do componente quando um componente [!DNL `PageView.frametransition`] está definido como [!DNL `turn`] ou como [!DNL `auto`] em sistemas de desktop.

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
   <td colname="col2"> <p>A opacidade da sombra no intervalo de <span class="codeph"> 0</span> a <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> O sinalizador ( <span class="codeph"> 0</span> ou <span class="codeph"> 1</span>) que ativa e desativa a borda ao redor da página de viragem. </p> </td> 
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

[!DNL `40,909090,1,1,909090,FFFFFF`]

## Exemplos {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]
