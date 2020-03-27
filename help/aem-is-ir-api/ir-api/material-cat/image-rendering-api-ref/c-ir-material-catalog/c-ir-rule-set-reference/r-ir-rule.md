---
description: Solicitar elemento de regra. Uma ou mais são opcionais no elemento <conjunto de regras>.
seo-description: Solicitar elemento de regra. Uma ou mais são opcionais no elemento <conjunto de regras>.
seo-title: regra
solution: Experience Manager
title: regra
topic: Scene7 Image Serving - Image Rendering API
uuid: f7071681-e97e-4081-aeb1-093d2b23041c
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# regra{#rule}

Solicitar elemento de regra. Uma ou mais são opcionais no `<ruleset>` elemento.

## Atributos {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"` Opcional. O padrão é &quot;break&quot;.

` Name=" *`text`*"` Optional. Usado para identificar o `<rule>` elemento nos registros de depuração e nas mensagens de erro.

Além disso, `<rule>` os elementos podem definir qualquer um dos atributos seguintes em qualquer combinação. Se especificado, e a regra for correspondida com êxito, eles substituirão os atributos de catálogo correspondentes para essa solicitação.

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Atributo &lt;regra&gt; </p> </th> 
   <th colname="col2" class="entry"> <p>Atributo do Catálogo de imagens correspondente </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DefaultPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local"> atributo::DefaultPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ErrorImage </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local"> atributo::ErrorImage </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Expiração </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local"> atributo::Expiração </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MaxPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local"> atributo::MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RootUrl </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local"> atributo::RootUrl </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte a descrição do atributo correspondente do catálogo de imagens para obter detalhes.

O atributo Expiration somente substitui o valor padrão do atributo; é ignorado se um `catalog::Expiration` valor específico se aplica à solicitação.

## Dados {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;expressão&gt; </span> </p> </td> 
  <td class="stentry"> <p>Opcional. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;substituição&gt; </span> </p> </td> 
  <td class="stentry"> <p>Opcional. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;enderesfilter&gt; </span> </p> </td> 
  <td class="stentry"> <p>Opcional. </p> </td> 
 </tr> 
</table>

## Notas {#section-a27b91f9a03047c0bb7edc0967fb4216}

Se ambos `<expression>` e `<substitution>` forem especificados e as subsequências capturadas não forem usadas, a primeira subsequência de caracteres correspondente será substituída por `<substitution>`.

Se não `<expression>` for especificado, qualquer caminho corresponderá e `<substitution>` será anexado ao final do caminho.

Se não `<substitution>` for especificado, a subsequência de caracteres correspondente será removida.

A regra `<addressfilter>` é aplicada somente quando ocorre uma correspondência e antes da aplicação das regras de query.
