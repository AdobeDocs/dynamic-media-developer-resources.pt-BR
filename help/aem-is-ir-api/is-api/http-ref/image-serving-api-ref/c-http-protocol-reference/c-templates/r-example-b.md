---
description: Requisitos semelhantes aos do Exemplo A, mas usam um fundo de cor sólida e permitem que a altura do composto varie, para acomodar imagens com diferentes proporções.
seo-description: Requisitos semelhantes aos do Exemplo A, mas usam um fundo de cor sólida e permitem que a altura do composto varie, para acomodar imagens com diferentes proporções.
seo-title: Exemplo B
solution: Experience Manager
title: Exemplo B
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 13120562-9201-4733-bd9d-4a54eac913e9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# Exemplo B{#example-b}

Requisitos semelhantes aos do Exemplo A, mas usam um fundo de cor sólida e permitem que a altura do composto varie, para acomodar imagens com diferentes proporções.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catálogo::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catálogo:Modificador</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+go+here&amp; layer=0&amp;size=800,0&amp;estender=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...$text$..rtf-encoding&amp;rotate=-90&amp;origin N=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

A imagem é colocada na camada 0 e o valor de altura `size=` é definido como 0, o que faz com que a altura real seja determinada pela altura da imagem depois de dimensioná-la para 800 pixels de largura.

`extend=` adiciona 100 pixels à parte superior e inferior e 200 pixels à direita.

As origens das camadas 0 e 1 são colocadas no centro direito da área de composição para alcançar a posição de texto desejada.

A ilustração a seguir mostra o resultado composto para diferentes proporções da imagem e diferentes strings de texto.

![](assets/exampleb.png)

