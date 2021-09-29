---
description: Requisitos semelhantes como o Exemplo A, mas usam um fundo de cor sólida e permitem que a altura do composto varie, para acomodar imagens com proporções diferentes.
solution: Experience Manager
title: Exemplo B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Exemplo B{#example-b}

Requisitos semelhantes como o Exemplo A, mas usam um fundo de cor sólida e permitem que a altura do composto varie, para acomodar imagens com proporções diferentes.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catálogo::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catálogo:Modificador</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+go+here&amp; layer=0&amp;size=800,0&amp;estender=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf..$text$..rtf-encoding&amp;rotate=-90&amp;origin N=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

A imagem é colocada na camada 0 e o valor de altura `size=` é definido como 0. Essa configuração faz com que a altura real seja determinada pela altura da imagem após dimensioná-la para 800 pixels de largura.

A variável `extend=` adiciona 100 pixels à parte superior e inferior e 200 pixels à direita.

As origens da camada 0 e da camada 1 são colocadas no centro direito da área de composição, para alcançar a posição de texto desejada.

A imagem a seguir mostra o resultado composto para diferentes proporções da imagem e diferentes sequências de texto.

![Exemplo de imagem B](assets/exampleb.png)
