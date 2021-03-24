---
description: A sombra da camada de estilo Photoshop e os efeitos de brilho são implementados usando subcamadas especiais (camadas de efeito) que podem ser anexadas a qualquer camada (a camada pai), incluindo layer=0 e layer=comp.
solution: Experience Manager
title: Efeitos da camada
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---


# Efeitos de camada{#layer-effects}

A sombra da camada de estilo Photoshop e os efeitos de brilho são implementados usando subcamadas especiais (camadas de efeito) que podem ser anexadas a qualquer camada (a camada pai), incluindo layer=0 e layer=comp.

Embora as camadas de efeito sejam compatíveis com vários atributos e comandos padrão de imagem e camada, elas não se destinam a camadas de propósito geral e não são compatíveis com dados independentes de imagem ou texto.

Qualquer número de efeitos de camada pode ser anexado a uma única camada pai.

## Efeitos internos e externos {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Os* efeitos internos são renderizados na parte superior da camada pai e são visíveis apenas em áreas opacas da camada pai. *Os* efeitos externos são renderizados atrás da camada pai (dessa forma, eles nunca serão visíveis em áreas opacas da camada pai) e podem ser posicionados em qualquer lugar dentro da tela de composição. Um efeito interno ou externo é escolhido atribuindo um número de camada de efeito positivo ou negativo com o comando `effect=`. O comando `effect=` também controla a ordenação z entre várias camadas de efeito anexadas à mesma camada pai.

## Relação com a camada principal {#section-eb8bfc4f754a42fc973b562821d6f2d3}

As camadas de efeito são dimensionadas e posicionadas automaticamente para coincidir com a camada pai (ou seja, a camada de efeito herda os valores `size=` e `origin=` da camada pai). `pos=` pode ser usada para afastar a camada de efeito da camada pai, como é normalmente necessário para efeitos de sombra interna e de sombra. Enquanto para camadas padrão `pos=` especifica um deslocamento entre as origens dessa camada e da camada 0, para camadas de efeito `pos=` especifica o deslocamento entre as origens da camada de efeito e da camada pai.

## Comandos e atributos compatíveis {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

As camadas de efeito aceitam os seguintes comandos e atributos:

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

Todos os outros comandos de imagem e camada contidos nas camadas de efeito são ignorados.

## Macros de efeito padrão {#section-a01e8dcc87c94495b54a6dfb21d2a718}

Para facilitar o uso de efeitos de camada, o IS fornece duas macros com o catálogo de imagem padrão, `$shadow$` e `$glow$`, que fornecem valores padrão para atributos de camada de efeito semelhantes aos efeitos de camada do Photoshop. A tabela a seguir lista qual efeito o comando e a macro devem ser usados para implementar os efeitos de camada padrão. Naturalmente, qualquer um dos atributos especificados nas macros pode ser modificado no URL ou macros alternativas podem ser criadas para implementar efeitos de camada personalizados.

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Efeito desejado</b> </th> 
   <th class="entry"> <b> Comando</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Sombra </p> </td> 
   <td> <p> <span class="codeph"> efeito=-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Sombra interna </p> </td> 
   <td> <p> <span class="codeph"> efeito=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Brilho externo </p> </td> 
   <td> <p> <span class="codeph"> efeito=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Brilho interno </p> </td> 
   <td> <p> <span class="codeph"> efeito=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplos {#section-4c449fdf707b43858917fb271fa1fe96}

Adicione uma borda vermelha de três pixels de largura com 50% de opacidade a uma camada:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

A borda seguirá os contornos do canal alfa ou da máscara da imagem. Em vez disso, definir `effect=1` colocaria a borda interna.

Adicione uma sombra suspensa azulada a uma imagem, usando as configurações de efeito padrão (exceto para a cor):

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` adiciona uma pequena margem às margens inferiores direita da imagem, o que impede que a sombra seja cortada nos limites da imagem.

## Consulte também {#section-1acccccf534549aea23d4c008c17e7c0}

[efeito=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), Macros  [de comando%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
