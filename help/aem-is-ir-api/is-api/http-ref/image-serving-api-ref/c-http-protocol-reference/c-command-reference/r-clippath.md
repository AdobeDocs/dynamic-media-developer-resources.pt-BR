---
description: Caminho do clipe de camada. Especifica um caminho de clipe para a camada atual.
seo-description: Caminho do clipe de camada. Especifica um caminho de clipe para a camada atual.
seo-title: clipPath
solution: Experience Manager
title: clipPath
uuid: fe84cf7a-63af-47d3-ae4f-2122f2f0a262
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 0%

---


# clipPath{#clippath}

Caminho do clipe de camada. Especifica um caminho de clipe para a camada atual.

`clipPath= *`pathDefinition`*`

`clipPathE= *``*&#42;[, *`pathNameName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Dados do caminho. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Nome do caminho incorporado na imagem de origem da camada (somente ASCII). </p></td> 
 </tr> 
</table>

Todas as partes da camada que se encaixam fora da área definida por `clipPath=` são renderizadas de forma transparente.

`*``*` pathName é o nome de um caminho incorporado na imagem de origem da camada. O caminho é automaticamente transformado para manter o alinhamento relativo com o conteúdo da imagem. Se mais de um `*`pathName`*` for especificado, o servidor recortará a imagem até a interseção desses caminhos. Qualquer `*`pathName`*` não encontrado na imagem de origem é ignorado.

>[!NOTE]
>
>Somente cadeias de caracteres ASCII são suportadas para `*`pathName`*`.

`*``*` pathDefinition permite especificar dados de caminho explícitos em coordenadas de pixel de camada.

Se `size=` for especificado e não for 0,0, a camada será pré-dimensionada. Nesse caso, as coordenadas de caminho são relativas ao canto superior esquerdo do retângulo de camada e a camada é posicionada com base em `origin=` ou em seu padrão. Todas as regiões do caminho fora do retângulo da camada permanecem transparentes.

Se `size=` não for especificado para uma cor sólida ou camada de texto, a camada será considerada de autodimensionamento com a extensão do caminho que determina seu tamanho. Se `origin=` não for especificado, o padrão será (0,0) do espaço de coordenadas de caminho. Isso permite que as coordenadas de caminho sejam especificadas em relação à origem da camada 0.

>[!NOTE]
>
>`scale=`Os  `rotate=`comandos ,  `anchor=`  e não são permitidos para camadas de cores sólidas de autodimensionamento.

`*``*` pathDefinition aceita uma string semelhante ao valor do  `d=` atributo do  `<path>` elemento SVG, exceto que vírgulas são usadas em vez de espaços para separar valores. `*``*` pathDefinition pode incluir um ou mais subcaminhos de ciclo fechado.

Os seguintes comandos de caminho são suportados em `*`pathDefinition`*`:

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Comando</b> </th> 
   <th class="entry"> <b> Nome</b> </th> 
   <th class="entry"> <b> Descrição</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> Mx,y</span> </td> 
   <td> <p> em absoluto </p> </td> 
   <td> <p> Inicie um novo subcaminho em x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> mx,y</span> </td> 
   <td> <p> movimento relativo </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> valor absoluto </p> </td> 
   <td> <p> Desenha uma linha da posição atual para x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto relativo </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto absoluto </p> </td> 
   <td> <p> Desenhe uma curva de Bezier da posição atual para x,y. x1,y1 é o ponto de controlo no início da curva e x2,y2 é o ponto de controlo no final da curva. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto relativo </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> |  <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> Feche o subcaminho atual com uma linha reta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Comandos em maiúsculas indicam que os valores de coordenada estão em posições de pixel absolutas (em relação à parte superior esquerda do retângulo de camada). Os deslocamentos de pixels seguem comandos em minúsculas em relação à posição atual.

&#39;m&#39; ou &#39;M&#39; sempre inicia um novo subcaminho. Os subcaminhos são fechados automaticamente (com uma linha reta) se &#39;Z&#39; ou &#39;z&#39; não forem especificados no final.

Se um subcaminho começar com um movimento relativo (&#39;m&#39;), ele será relativo a um dos seguintes:

* O ponto inicial do subcaminho anterior, se ele foi fechado com &#39;z&#39; ou &#39;Z&#39;.
* O ponto final do subcaminho anterior, se ele não tiver sido fechado explicitamente.
* 0,0, se este for o primeiro subcaminho.

## Propriedades {#section-d4127db0dac54e3cbd44f7ea1e001960}

Atributo de camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. As camadas de efeito ignoram-no.

`clipPathE=` é ignorada se nenhum caminho com o nome especificado for encontrado na imagem de origem da camada ou se a origem da camada não for uma imagem.

## Padrão {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Nenhum, para nenhum recorte adicional da camada.

## Consulte também {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ,  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ,  [estender=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
