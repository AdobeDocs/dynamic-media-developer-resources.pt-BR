---
description: Solicitar elemento de regra. Uma ou mais regras são opcionais no elemento <ruleset> .
seo-description: Solicitar elemento de regra. Uma ou mais regras são opcionais no elemento <ruleset> .
seo-title: regra
solution: Experience Manager
title: regra
uuid: 8b8e5b06-a0b7-47e1-942d-0297d08c313b
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 2%

---


# rule{#rule}

Solicitar elemento de regra. Uma ou mais regras são opcionais no elemento `<ruleset>` .

## Atributos {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"`: Opcional. O padrão é &quot;break&quot;.

`Replace = "first" | "all"`: Opcional. O padrão é &quot;primeiro&quot;.

`RequestType` =  *&quot;`types`&quot;*: Opcional. Especifica a qual contexto de entrada a regra se aplica. *`types`* é uma lista separada por vírgulas, que pode incluir um ou mais tokens listados na tabela a seguir. Se `RequestType` não for especificado, a regra se aplica às solicitações recebidas em todos os contextos compatíveis.

<table id="table_4935E1ED03624DA6AF3F8DC9AAA10237"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><b>token</b> </p> </th> 
   <th class="entry"> <p><b>Contexto</b> </p> </th> 
   <th class="entry"> <p><b>Descrição</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> é</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/image/</span> </p> </td> 
   <td> <p>Aplicado às solicitações de exibição de imagem </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ir</span> </p> </td> 
   <td> <p> <span class="filepath"> /ir/render/</span> </p> </td> 
   <td> <p>Aplicado às solicitações de renderização de imagem </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> estático</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/content/</span> </p> </td> 
   <td> <p>Aplicado a solicitações de conteúdo estático </p> </td> 
  </tr> 
 </tbody> 
</table>

**`Name = "text"`**: Opcional. Usado para identificar o elemento `<rule>` em logs de depuração e mensagens de erro.

`  *`Atributo`* ="value"`: Opcional. `<rule>` Os elementos podem definir qualquer um dos atributos a seguir em qualquer combinação. Se especificado, e a regra for correspondida com êxito, eles substituirão os atributos de catálogo correspondentes para esta solicitação. O padrão é `RequestType="is"`.

<table id="table_67AED5BEADDF4DAC99B5EF46438C1ABC"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <span class="varname"> Atributo  </span> </b> </th> 
   <th class="entry"> <p>Atributo de catálogo de imagem correspondente </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> DefaultImageMode</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local"> atributo::DefaultImageMode</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ErrorImage</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"> atributo::ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Expiração</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local"> atributo::Expiration</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MaxPix</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> atributo::MaxPix  </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestLock</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"> atributo::RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestObfuscation</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local"> atributo::RequestObfuscation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RootUrl</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> atributo::RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> SavePath</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local"> atributo::SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MarcaÁgua</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local"> atributo::WaterMark</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte a descrição do atributo do catálogo de imagens correspondente para obter detalhes.

Os atributos Expiration substituem apenas os valores de atributo padrão. A substituição será ignorada se um valor `catalog::Expiration` específico se aplicar à solicitação.

## Dados {#section-8fce013a4c724da58af3fee4e7a90e72}

<table id="simpletable_4F1C03671DA942A3A332B2C686A63C52"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;expression&gt;</span> </p></td> 
  <td class="stentry"> <p>Opcional </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;substitution&gt;</span> </p></td> 
  <td class="stentry"> <p>Opcional </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;addressfilter&gt;</span> </p></td> 
  <td class="stentry"> <p>Opcional </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;header&gt;</span> </p></td> 
  <td class="stentry"> <p>Opcional </p></td> 
 </tr> 
</table>

## Notas {#section-0c5fbc363070419d8c9800b0c02dc9f9}

Se `<expression>` e `<substitution>` forem especificadas e as subsequências capturadas não forem usadas, a primeira subsequência correspondente será substituída por `<substitution>`.

Se `<expression>` não for especificado, qualquer caminho corresponderá e `<substitution>` será anexado ao final do caminho.

Se `<substitution>` não for especificado, nenhuma transformação de caminho ou consulta ocorrerá, mas todos os atributos de catálogo especificados serão substituídos. Se `<substitution>` estiver vazio, a substring correspondente será removida.

O `<addressfilter>` é aplicado somente quando ocorre uma correspondência e antes da aplicação das regras de consulta.
