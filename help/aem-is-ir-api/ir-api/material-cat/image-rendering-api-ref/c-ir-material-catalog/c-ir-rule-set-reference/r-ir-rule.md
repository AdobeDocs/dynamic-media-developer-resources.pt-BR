---
description: Elemento de regra de solicitação. Um ou mais são opcionais no elemento <ruleset>.
solution: Experience Manager
title: regra
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f56012c-d01c-489c-9d18-91e256f72012
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# regra{#rule}

Elemento de regra de solicitação. Um ou mais são opcionais no elemento `<ruleset>`.

## Atributos {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"` Opcional. O padrão é &quot;break&quot;.

` Name=" *`texto`*"` Opcional. Usado para identificar o elemento `<rule>` em logs de depuração e mensagens de erro.

Além disso, elementos `<rule>` podem definir qualquer um dos atributos a seguir em qualquer combinação. Se especificado, e a regra for correspondida com sucesso, eles substituirão os atributos de catálogo correspondentes para esta solicitação.

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>atributo &lt;rule&gt; </p> </th> 
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
   <td colname="col2"> <p> Atributo <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local">::ErrorImage </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Expiração </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local"> atributo::Expiration </a> </p> </td> 
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

Consulte a descrição do atributo de catálogo de imagens correspondente para obter detalhes.

O atributo Expiration substitui somente o valor de atributo padrão; ele é ignorado se um valor `catalog::Expiration` específico se aplicar à solicitação.

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
  <td class="stentry"> <p> <span class="codeph"> &lt;filtro_de_endereçamento&gt; </span> </p> </td> 
  <td class="stentry"> <p>Opcional. </p> </td> 
 </tr> 
</table>

## Notas {#section-a27b91f9a03047c0bb7edc0967fb4216}

Se `<expression>` e `<substitution>` forem especificados e as subsequências capturadas não forem usadas, a primeira subsequência correspondente será substituída por `<substitution>`.

Se `<expression>` não for especificado, qualquer caminho corresponderá e `<substitution>` será anexado ao final do caminho.

Se `<substitution>` não for especificado, a subcadeia correspondente será removida.

O `<addressfilter>` é aplicado somente quando ocorre uma correspondência e antes da aplicação das regras de consulta.
