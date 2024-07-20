---
description: Requisitos semelhantes ao do Exemplo A, mas usa um plano de fundo de cor sólida e permite que a altura do composto varie para acomodar imagens com diferentes taxas de proporção.
solution: Experience Manager
title: Exemplo B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# Exemplo B{#example-b}

Requisitos semelhantes ao do Exemplo A, mas usa um plano de fundo de cor sólida e permite que a altura do composto varie para acomodar imagens com diferentes taxas de proporção.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catálogo::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catálogo::Modificador</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $texto=camada+1+texto+vai+aqui&amp; camada=0&amp;tamanho=800,0&amp;estender=0,100,200,100&amp;src=$objeto$&amp;origemN=.5,0&amp; camada=1&amp;texto=rtf...$texto$...rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

A imagem é colocada na camada 0, e o valor da altura de `size=` é definido como 0. Essa configuração faz com que a altura real seja determinada pela altura da imagem após dimensioná-la para 800 pixels de largura.

A variável `extend=` adiciona 100 pixels à parte superior e inferior e 200 pixels à direita.

As origens das camadas 0 e 1 são colocadas no centro-direito da área de composição para atingir a posição de texto desejada.

A imagem a seguir mostra o resultado composto para diferentes taxas de proporção da imagem e diferentes cadeias de texto.

![Exemplo de imagem B](assets/exampleb.png)
