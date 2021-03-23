---
description: Tipo de solicitação. Especifica o tipo de dados solicitado.
seo-description: Tipo de solicitação. Especifica o tipo de dados solicitado.
seo-title: req
solution: Experience Manager
title: req
uuid: 9dd13338-3457-477f-96e7-3ace7266d0ab
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '973'
ht-degree: 0%

---


# req{#req}

Tipo de solicitação. Especifica o tipo de dados solicitado.

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> depurar  </span> </p> </td> 
  <td class="stentry"> <p>Execute comandos no modo de depuração. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> conteúdo  </span> </p> </td> 
  <td class="stentry"> <p>Retorne informações sobre os objetos na vinheta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img  </span> </p> </td> 
  <td class="stentry"> <p>Execute comandos e retorne a imagem renderizada. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops  </span> </p> </td> 
  <td class="stentry"> <p>Retorna as propriedades da vinheta especificada. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> mapa  </span> </p> </td> 
  <td class="stentry"> <p>Retorna os dados do mapa de imagem incorporados na vinheta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> objeto  </span> </p> </td> 
  <td class="stentry"> <p>Execute comandos e retorne a imagem renderizada à seleção de objeto atual. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> props  </span> </p> </td> 
  <td class="stentry"> <p>Execute comandos e retorne propriedades da imagem de resposta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> userdata  </span> </p> </td> 
  <td class="stentry"> <p>Retorna o conteúdo de <span class="codeph"> vinheta::UserData </span>. </p> </td> 
 </tr> 
</table>

Salvo indicação em contrário nas descrições detalhadas, o servidor retorna respostas de texto com o tipo MIME &lt;text/plain>.

`debug`

Executa os comandos especificados e retorna a imagem renderizada. Se ocorrer um erro, as informações de erro e depuração serão retornadas em vez da imagem de erro ( `attribute::ErrorImagePath`).

`contents`

Retorna uma representação XML da hierarquia de objetos na vinheta, incluindo os atributos de objeto selecionados. Outros comandos na solicitação são ignorados.

`img`

Executa os comandos especificados e retorna a imagem renderizada. O formato e o tipo de resposta dos dados de resposta são determinados por `fmt=`.

`imageprops`

Retorna as propriedades selecionadas do arquivo de vinheta ou entrada de catálogo especificado no caminho do URL. Consulte [Propriedades](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) para obter uma descrição da sintaxe de resposta e do tipo MIME de resposta. Outros comandos na solicitação são ignorados. As seguintes propriedades são retornadas:

<table id="table_A30296D29B5D43F1B5383A887252C6B4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Propriedade </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.expiration  </span> </p> </td> 
   <td colname="col2"> <p>Duplo </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Expiration  </span> ou o tempo padrão para a vida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td colname="col2"> <p>Número inteiro </p> </td> 
   <td colname="col3"> <p>Altura da resolução completa em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p>nome/descrição do perfil associado a esta vinheta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile  </span> </p> </td> 
   <td colname="col2"> <p>Booleano </p> </td> 
   <td colname="col3"> <p>1 se o perfil associado estiver incorporado na vinheta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths  </span> </p> </td> 
   <td colname="col2"> <p>Booleano </p> </td> 
   <td colname="col3"> <p>1 se a vinheta incorporar os dados de caminho. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier  </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Modifier  </span> ou empty se não for uma entrada de catálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixType  </span> </p> </td> 
   <td colname="col2"> <p>Enum </p> </td> 
   <td colname="col3"> <p>Tipo de pixel da imagem de resposta; pode ser 'CMYK', 'RGB' ou 'BW' (para imagens em tons de cinza). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolução de impressão padrão em dpi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp  </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p>Data/hora de modificação (do <span class="codeph"> catálogo::TimeStamp </span> ou do arquivo de vinheta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td colname="col2"> <p>Número inteiro </p> </td> 
   <td colname="col3"> <p>Largura da resolução completa em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vinheta.name  </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p>Nome da vinheta (sequência de nome do objeto da vinheta raiz). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vinheta.res  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolução máxima do objeto em <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> resolução do material </a> unidades (normalmente pixels/polegada). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vinheta.res.avg  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolução média de objeto em <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> unidades de resolução de material </a> (normalmente pixels/inc <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> resolução de material </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vinheta.res.min  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolução mínima do objeto em <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> unidades de resolução de material </a> (normalmente pixels/polegada). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vinheta.version  </span> </p> </td> 
   <td colname="col2"> <p>Número inteiro </p> </td> 
   <td colname="col3"> <p>Número de versão do arquivo Vignette. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

Retorna os dados do mapa de imagem incluídos na vinheta. Por padrão, os dados de mapa para todos os grupos mais externos são retornados. Os dados do mapa para todos os grupos mais internos podem ser obtidos com

`req=map&groupLevel=-1`

Os dados do mapa não são dimensionados para `wid=` ou `hei=` ou modificados de outra forma. O tipo MIME de resposta é `<text/xml>`.

Os dados de resposta consistem em um elemento `<map>` contendo um conjunto de elementos `<area>`, semelhante à tag HTML `<AREA>`.

Cada elemento `<area>` inclui os atributos padrão `type=` e `coord=`, bem como um atributo `name=`, especificando o nome do grupo de vinheta ou o caminho do nome. Vários elementos `<area>` com o mesmo nome estarão presentes se as máscaras do grupo de objetos correspondente tiverem regiões descontínuas.

Além dos atributos padrão, as vinhetas podem definir atributos adicionais se tiverem sido criadas. Esses atributos personalizados são definidos como atributos de grupo de objetos. Os nomes dos atributos personalizados devem começar com `map`. a ser incluído nos elementos `<area>`. Por exemplo, se os atributos de grupo incluírem `map.href=http://www.scene7.com`, o elemento `<area>` correspondente incluirá `href="http://www.scene7.com"`.

Um documento XML com um elemento `<map>` vazio será retornado se a vinheta não incluir dados de mapa.

`object`

Executa os comandos especificados e retorna a imagem renderizada mascarada pela seleção do objeto residual (o grupo ou objeto selecionado com o último comando `sel=` ou `obj=` na solicitação). Normalmente é usado em conjunto com um formato de imagem que suporta alfa (consulte [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)). Se for usado um formato de imagem que não suporta alfa, as áreas fora da máscara são pretas.

`props`

Executa os comandos especificados e retorna propriedades da vinheta e propriedades de grupo ou objeto, em vez da imagem renderizada. Consulte [Propriedades](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) para obter uma descrição da sintaxe de resposta e o tipo MIME de resposta. A seleção padrão se aplica a menos que `obj=` ou `sel=` também seja especificado (consulte [ `obj=` ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

As seguintes propriedades podem ser incluídas na resposta:

<table id="table_F3ECF0584F6247A2A75C1CAFE1C57A4E"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Propriedade </p> </th> 
   <th class="entry"> <p> Tipo </p> </th> 
   <th class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> image.bgc  </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Cor do fundo da imagem de resposta. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td> <p>Número inteiro </p> </td> 
   <td> <p> Responder altura da imagem em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed  </span> </p> </td> 
   <td> <p> Booleano </p> </td> 
   <td> <p>True se o perfil ICC for incorporado na imagem de resposta (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Nome do atalho do perfil associado à imagem de resposta (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask  </span> </p> </td> 
   <td> <p> Booleano </p> </td> 
   <td> <p> True se a imagem de resposta incluir alfa. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed  </span> </p> </td> 
   <td> <p> Booleano </p> </td> 
   <td> <p> True se a imagem de resposta incluir dados de caminho (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType  </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Tipo de imagem de resposta, pode ser 'CMYK', 'RGB' ou 'BW' (para imagens em tons de cinza) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td> <p> Real </p> </td> 
   <td> <p> Resolução de impressão (dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality  </span> </p> </td> 
   <td> <p>Número inteiro, booleano </p> </td> 
   <td> <p> Qualidade JPEG e sinalizador de croma (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type  </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Tipo MIME para a imagem de resposta (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td> <p> Número inteiro </p> </td> 
   <td> <p> Responder a largura da imagem em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes  </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Sequência de caracteres de atributos para a seleção atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count  </span> </p> </td> 
   <td> <p> Número inteiro </p> </td> 
   <td> <p> Número de objetos na seleção atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident  </span> </p> </td> 
   <td> <p> Número inteiro </p> </td> 
   <td> <p> Recuar valor da seleção atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selecione  <span class="codeph"> selection.attributes  </span>ion.name  </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Caminho do nome completo da seleção de objeto atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overlapping  </span> </p> </td> 
   <td> <p> Número inteiro </p> </td> 
   <td> <p> número de objetos de sobreposição na seleção atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable  </span> </p> </td> 
   <td> <p> Número inteiro </p> </td> 
   <td> <p>Número de objetos renderizáveis na seleção atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable  </span> </p> </td> 
   <td> <p> Número inteiro </p> </td> 
   <td> <p> Número de objetos texturizáveis na seleção atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible  </span> </p> </td> 
   <td> <p> Número inteiro </p> </td> 
   <td> <p> Status atual de mostrar/ocultar da seleção atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder  </span> </p> </td> 
   <td> <p> Número inteiro </p> </td> 
   <td> <p> Valor em ordem Z do primeiro objeto de sobreposição na seleção atual. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

Retorna o conteúdo de `vignette::UserData`. O servidor substituirá todas as ocorrências de `'??'` em `vignette::UserData` por terminadores de linha ( `<cr><lf>`). A resposta é formatada como dados de texto com o tipo MIME de resposta definido como &lt;text/plain>.

Se o objeto especificado no caminho do URL não for resolvido para uma entrada válida do mapa de vinheta, ou se `vignette::UserData` estiver vazio, a resposta conterá apenas um terminador de linha ( `CR/LF`).

Quaisquer outros comandos na cadeia de caracteres de solicitação são ignorados.

## Propriedades {#section-e44092e190ff4f6380583e8ed6ea5b0b}

comando Solicitar. Pode ocorrer em qualquer lugar na cadeia de caracteres de solicitação.

## Padrão {#section-00c593cbf1af4364b6b78812e6b93c64}

Se o URL não incluir um caminho de imagem ou modificadores, então:

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Caso contrário, `req=img`

## Consulte também {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) ,  [atributo::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0),  [vinheta::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85),  [Propriedades](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
