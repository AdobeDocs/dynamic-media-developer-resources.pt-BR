---
title: ajustar
description: Modo de Ajuste de Imagem de Resposta. Especifica como o fator de escala é calculado, que é usado para dimensionar a imagem composta para a imagem de resposta quando o tamanho da resposta é especificado com wid= e hei= e scl= não está presente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# ajustar{#fit}

Modo de Ajuste de Imagem de Resposta. Especifica como o fator de escala é calculado, que é usado para dimensionar a imagem composta para a imagem de resposta quando o tamanho da resposta é especificado com wid= e hei= e scl= não está presente.

` fit= *`modo`*, *`upscale`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modo </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ajustar|restringir|cortar|quebrar|esticar|ajuste|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> upscale </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
 </tr> 
</table>

Na descrição a seguir das opções de modo, presume-se que *`xScale`* é a relação entre a largura da imagem composta e a largura da imagem de resposta e *`yScale`* é a relação entre a altura da imagem composta e a altura da imagem de resposta.

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parâmetro </th> 
   <th colname="col2" class="entry"> Definição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> ajustar </span> </p> </td> 
   <td colname="col2"> <p>Dimensiona a imagem composta para que ela se ajuste ao espaço alocado com <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>, com espaço em branco mínimo e sem corte. A imagem de resposta tem o tamanho exato especificado com <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>. O menor dos <span class="varname"> xScale </span> e <span class="varname"> yScale </span> é aplicada. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> restringir </span> </p> </td> 
   <td colname="col2"> <p>Dimensiona a imagem composta como <span class="codeph"> ajustar </span> para que se encaixe no espaço alocado com <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>, mas a imagem de resposta real pode ser menor do que o especificado com <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span> para evitar espaços em branco. O menor dos <span class="varname"> xScale </span> e <span class="varname"> yScale </span> é aplicada. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> cortar </span> </p> </td> 
   <td colname="col2"> <p>Dimensiona a imagem composta para que ela preencha toda a imagem de resposta, com recorte mínimo e sem espaços em branco. O maior dos <span class="varname"> xScale </span> e <span class="varname"> yScale </span> é aplicada. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> quebra automática </span> </p> </td> 
   <td colname="col2"> <p>Dimensiona a imagem composta como <span class="codeph"> cortar </span> para que cubra toda a imagem de resposta, mas a imagem de resposta real pode ser maior do que o especificado com <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span> para evitar o corte. O maior dos <span class="varname"> xScale </span> e <span class="varname"> yScale </span>é aplicada. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> esticar </span> </p> </td> 
   <td colname="col2"> <p>Dimensiona a imagem composta independentemente em x e y para preencher toda a imagem de resposta, sem recorte e sem espaços em branco. Isso normalmente altera a proporção da imagem. <span class="varname"> xScale </span> é usado para dimensionamento horizontal e <span class="varname"> yScale </span> para dimensionamento vertical. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hit </span> </p> </td> 
   <td colname="col2"> <p>Aplica <span class="varname"> xScale </span> para ajustar firmemente a imagem horizontalmente, provavelmente cortando ou deixando espaço em branco na parte superior e/ou inferior. Útil para aplicações especiais. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>Aplica <span class="varname"> yScale </span> para ajustar firmemente a imagem verticalmente, provavelmente com cortes ou espaços em branco à esquerda e/ou direita. Útil para aplicações especiais. </p> </td> 
  </tr> 
 </tbody> 
</table>

Definir *`upscale`* para &#39;1&#39; para permitir o upscaling ou para &#39;0&#39; para restringir *`xScale`*e *`yScale`* ser limitado a 1:1. Se o upscaling estiver desativado, espaços em branco adicionais poderão estar presentes se a imagem composta for menor que a imagem de resposta.

O corte e o espaço em branco são centralizados por padrão; sua posição pode ser controlada com `align=`. A cor e a opacidade do preenchimento de espaço em branco são determinadas por `bgc=`.

## Propriedades {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Exibir atributo. Aplica-se independentemente da configuração da camada atual. Pelo menos um de `wid=` ou `hei=` também deve ser especificado, caso contrário, um erro será retornado; ambos `wid=` e `hei=` deve ser especificado para que os modos de ajuste se comportem conforme descrito. Um erro é retornado quando `req=tmb` também é especificado.

## Padrão {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Consulte também {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
