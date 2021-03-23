---
description: Modo de ajuste da imagem de resposta. Especifica como o fator de escala é calculado, que é usado para dimensionar a imagem composta para a imagem de resposta quando o tamanho de resposta é especificado com wid= e hei= e scl= não está presente.
seo-description: Modo de ajuste da imagem de resposta. Especifica como o fator de escala é calculado, que é usado para dimensionar a imagem composta para a imagem de resposta quando o tamanho de resposta é especificado com wid= e hei= e scl= não está presente.
seo-title: ajuste
solution: Experience Manager
title: ajuste
uuid: 669fe757-f3a1-4cd4-b46c-6fbe5a039ce0
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---


# fit{#fit}

Modo de ajuste da imagem de resposta. Especifica como o fator de escala é calculado, que é usado para dimensionar a imagem composta para a imagem de resposta quando o tamanho de resposta é especificado com wid= e hei= e scl= não está presente.

` fit= *``*, *`modeupscale`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modo  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|constrain|cortar|quebra|esticar|hfit|vfit  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> expansão  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
 </tr> 
</table>

Na seguinte descrição das opções de modo, presume-se que *`xScale`* é a proporção da largura da imagem composta com a largura da imagem de resposta e *`yScale`* é a proporção da altura da imagem composta com a altura da imagem de resposta.

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parâmetro </th> 
   <th colname="col2" class="entry"> Definição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> ajuste  </span> </p> </td> 
   <td colname="col2"> <p>Dimensiona a imagem composta de forma que se ajuste ao espaço alocado com <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>, com espaço em branco mínimo e sem recorte. A imagem de resposta terá o tamanho exato especificado com <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>. O menor de <span class="varname"> xScale </span> e <span class="varname"> Scale </span> é aplicado. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> restringir  </span> </p> </td> 
   <td colname="col2"> <p>Dimensiona a imagem composta como <span class="codeph"> ajuste </span> para que se encaixe no espaço alocado com <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>, mas a imagem de resposta real pode ser menor do que o especificado com <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span> para evitar espaços em branco. O menor de <span class="varname"> xScale </span> e <span class="varname"> Scale </span> é aplicado. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> cultura  </span> </p> </td> 
   <td colname="col2"> <p>Dimensiona a imagem composta de forma que ela preencha a imagem de resposta inteira, com o corte mínimo e sem espaço em branco. Aplica-se o maior de <span class="varname"> xScale </span> e <span class="varname"> Scale </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> quebra  </span> </p> </td> 
   <td colname="col2"> <p>Dimensiona a imagem composta como <span class="codeph"> recortar </span> de forma que cubra toda a imagem de resposta, mas a imagem de resposta real pode ser maior do que o especificado com <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span> para evitar o corte. Aplica-se o maior de <span class="varname"> xScale </span> e <span class="varname"> Scale </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> esticar  </span> </p> </td> 
   <td colname="col2"> <p>Dimensiona a imagem composta de maneira independente em x e y para preencher a imagem de resposta inteira, sem corte e sem espaço em branco. Isso normalmente altera a proporção de aspecto da imagem. <span class="varname"> xScale  </span> é usado para dimensionamento horizontal e  <span class="varname"> yScale  </span> para dimensionamento vertical. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hino  </span> </p> </td> 
   <td colname="col2"> <p>Aplica <span class="varname"> xScale </span> para ajustar firmemente a imagem na horizontal, com o corte provável ou espaço em branco na parte superior e/ou inferior. Útil para aplicativos especiais. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vaso  </span> </p> </td> 
   <td colname="col2"> <p>Aplica <span class="varname"> Escala </span> para ajustar firmemente a imagem na vertical, com provável corte ou espaço em branco à esquerda e/ou à direita. Útil para aplicativos especiais. </p> </td> 
  </tr> 
 </tbody> 
</table>

Defina *`upscale`* como &#39;1&#39; para permitir que a expansão ou como &#39;0&#39; restrinja *`xScale`*e *`yScale`* sejam limitadas a 1:1. Se a expansão estiver desativada, o espaço em branco adicional poderá estar presente se a imagem composta for menor que a imagem de resposta.

O comando Recortar e o espaço em branco são centralizados por padrão; sua posição pode ser controlada com `align=`. A cor e a opacidade do preenchimento do espaço em branco são determinadas por `bgc=`.

## Propriedades {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Exibir atributo. Aplica-se independentemente da configuração de camada atual. Pelo menos um de `wid=` ou `hei=` também deve ser especificado, caso contrário, um erro é retornado; `wid=` e `hei=` devem ser especificadas para que os modos de ajuste se comportem conforme descrito. Um erro é retornado quando `req=tmb` também é especificado.

## Padrão {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Consulte também {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
