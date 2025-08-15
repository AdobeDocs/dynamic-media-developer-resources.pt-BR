---
title: clipPath
description: Caminho do clipe de camada. Especifica um caminho de recorte para a camada atual.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# clipPath{#clippath}

Caminho do clipe de camada. Especifica um caminho de recorte para a camada atual.

`clipPath= *`definiçãoCaminho`*`

`clipPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Dados de caminho. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Nome do caminho incorporado na imagem de origem da camada (somente ASCII). </p></td> 
 </tr> 
</table>

Qualquer parte da camada que esteja fora da área definida por `clipPath=` é renderizada transparente.

`*`pathName`*` é o nome de um caminho incorporado na imagem de origem da camada. O caminho é transformado automaticamente para manter o alinhamento relativo com o conteúdo da imagem. Se mais de um `*`pathName`*` for especificado, o servidor recortará a imagem na interseção desses caminhos. Qualquer `*`pathName`*` não encontrado na imagem de origem será ignorado.

>[!NOTE]
>
>Há suporte somente para cadeias de caracteres ASCII para `*`pathName`*`.

`*`pathDefinition`*` permite especificar dados de caminho explícitos em coordenadas de pixel de camada.

Se `size=` for especificado e não 0,0, a camada será pré-dimensionada. Nesse caso, as coordenadas do caminho são relativas ao canto superior esquerdo do retângulo da camada e a camada é posicionada com base em `origin=` ou em seu padrão. Todas as regiões do caminho fora do retângulo de camada permanecem transparentes.

Se `size=` não for especificado para uma camada de texto ou cor sólida, a camada será considerada autodimensionável com a extensão do caminho determinando seu tamanho. Se `origin=` não for especificado, o padrão será (0,0) do espaço de coordenadas do caminho. Esse processo de fluxo de trabalho permite que coordenadas de caminho sejam especificadas de acordo com a origem da camada 0.

>[!NOTE]
>
>Os comandos `scale=`, `rotate=` e `anchor=` não são permitidos para camadas de cores sólidas de autodimensionamento.

`*`pathDefinition`*` aceita uma cadeia de caracteres semelhante ao valor do atributo `d=` do elemento `<path>` do SVG, exceto que são usadas vírgulas em vez de espaços para separar valores. `*`pathDefinition`*` pode incluir um ou mais subcaminhos de ciclo fechado.

Os seguintes comandos de caminho têm suporte em `*`pathDefinition`*`:

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
   <td> <b> M</b> <span class="varname"> x, y</span> </td> 
   <td> <p> mover para absoluto </p> </td> 
   <td> <p> Iniciar um novo subcaminho em x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x, y</span> </td> 
   <td> <p> mover para relativo </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> absoluto de lineto </p> </td> 
   <td> <p> Desenhe uma linha da posição atual para x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto relativo </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto absoluto </p> </td> 
   <td> <p> Desenhe uma curva de Bézier da posição atual para x,y. x1,y1 é o ponto de controle no início da curva e x2,y2 é o ponto de controle no final da curva. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> Fechar o subcaminho atual com uma linha reta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Comandos em maiúsculas indicam que os valores de coordenadas estão em posições absolutas de pixel (relativas ao canto superior esquerdo do retângulo da camada). Os deslocamentos de pixels seguem comandos em minúsculas em relação à posição atual.

&#39;m&#39; ou &#39;M&#39; sempre inicia um novo subcaminho. Os subcaminhos são fechados automaticamente (com uma linha reta) se &#39;Z&#39; ou &#39;z&#39; não for especificado no final.

Se um subcaminho começar com um moveto relativo (&#39;m&#39;), ele será relativo a um dos seguintes:

* O ponto inicial do subcaminho anterior, se ele foi fechado com &#39;z&#39; ou &#39;Z&#39;.
* O ponto final do subcaminho anterior, se ele não foi fechado explicitamente.
* 0,0, se for o primeiro subcaminho.

## Propriedades {#section-d4127db0dac54e3cbd44f7ea1e001960}

Atributo de camada. Aplica-se à camada atual ou à imagem composta, se `layer=comp`. As camadas de efeito o ignoram.

O modificador `clipPathE=` será ignorado se nenhum caminho com o nome especificado for encontrado na imagem de origem da camada, ou se a origem da camada não for uma imagem.

## Padrão {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Nenhum, para nenhum recorte adicional da camada.

## Consulte também {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
