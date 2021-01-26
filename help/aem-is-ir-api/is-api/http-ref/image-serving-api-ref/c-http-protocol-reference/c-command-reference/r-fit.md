---
description: Modo de ajuste de imagem de resposta. Especifica como o fator de escala é calculado, que é usado para dimensionar a imagem composta para a imagem de resposta quando o tamanho de resposta é especificado com wid= e hei= e scl= não está presente.
seo-description: Modo de ajuste de imagem de resposta. Especifica como o fator de escala é calculado, que é usado para dimensionar a imagem composta para a imagem de resposta quando o tamanho de resposta é especificado com wid= e hei= e scl= não está presente.
seo-title: ajuste
solution: Experience Manager
title: ajuste
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 669fe757-f3a1-4cd4-b46c-6fbe5a039ce0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---


# fit{#fit}

Modo de ajuste de imagem de resposta. Especifica como o fator de escala é calculado, que é usado para dimensionar a imagem composta para a imagem de resposta quando o tamanho de resposta é especificado com wid= e hei= e scl= não está presente.

` fit= *`escala `*, *`moderna`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modo  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ajustar|restringir|recortar|quebra|estiramento|ajuste|vfit  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> escala  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
 </tr> 
</table>

Na seguinte descrição das opções de modo, presume-se que *`xScale`* é a proporção entre a largura da imagem composta e a largura da imagem de resposta e *`yScale`* é a proporção entre a altura da imagem composta e a altura da imagem de resposta.

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
   <td colname="col2"> <p>Dimensiona a imagem composta para que se ajuste ao espaço alocado com <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>, com espaço em branco mínimo e sem recorte. A imagem de resposta terá o tamanho exato especificado com <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>. É aplicado o menor valor de <span class="varname"> xScale </span> e <span class="varname"> yScale </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> restrição  </span> </p> </td> 
   <td colname="col2"> <p>Dimensiona a imagem composta como <span class="codeph"> ajuste </span> para que se ajuste ao espaço alocado com <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>, mas a imagem de resposta real pode ser menor do que a especificada com <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span> para evitar espaços em branco. É aplicado o menor valor de <span class="varname"> xScale </span> e <span class="varname"> yScale </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> cultura  </span> </p> </td> 
   <td colname="col2"> <p>Dimensiona a imagem composta para que ela preencha a imagem de resposta inteira, com o mínimo de corte e nenhum espaço em branco. O maior de <span class="varname"> xScale </span> e <span class="varname"> yScale </span> é aplicado. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> moldura  </span> </p> </td> 
   <td colname="col2"> <p>Dimensiona a imagem composta como <span class="codeph"> recorte </span> para que ela cubra toda a imagem de resposta, mas a imagem de resposta real pode ser maior do que o especificado com <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span> para evitar recortes. Aplica-se o maior de <span class="varname"> xScale </span> e <span class="varname"> yScale </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> extensão  </span> </p> </td> 
   <td colname="col2"> <p>Dimensiona a imagem composta independentemente em x e y para preencher a imagem de resposta inteira, sem cortes e sem espaços em branco. Normalmente, isso muda a proporção da imagem. <span class="varname"> O xScale  </span> é usado para dimensionamento horizontal e  <span class="varname"> yScale  </span> para dimensionamento vertical. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> capacete  </span> </p> </td> 
   <td colname="col2"> <p>Aplica <span class="varname"> xScale </span> para ajustar firmemente a imagem horizontalmente, com provável corte ou espaço em branco na parte superior e/ou inferior. Útil para aplicativos especiais. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vaso  </span> </p> </td> 
   <td colname="col2"> <p>Aplica <span class="varname"> yScale </span> para ajustar firmemente a imagem na vertical, com provável corte ou espaço em branco à esquerda e/ou à direita. Útil para aplicativos especiais. </p> </td> 
  </tr> 
 </tbody> 
</table>

Defina *`upscale`* como &#39;1&#39; para permitir a expansão ou como &#39;0&#39; para restringir *`xScale`*e *`yScale`* a 1:1. Se a ampliação estiver desativada, um espaço em branco adicional poderá estar presente se a imagem composta for menor que a imagem de resposta.

O espaço em branco e de corte estão centralizados por padrão; sua posição pode ser controlada com `align=`. A cor e a opacidade do preenchimento do espaço em branco são determinadas por `bgc=`.

## Propriedades {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Atributo de visualização. Aplica-se independentemente da configuração de camada atual. Pelo menos um de `wid=` ou `hei=` também deve ser especificado, caso contrário, um erro será retornado; `wid=` e `hei=` devem ser especificados para que os modos de ajuste se comportem conforme descrito. Um erro é retornado quando `req=tmb` também é especificado.

## Padrão {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Consulte também {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [alinhamento=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
