---
title: solic
description: Tipo de solicitação. Especifica o tipo de dados solicitados.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 0%

---

# solic{#req}

Tipo de solicitação. Especifica o tipo de dados solicitados.

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> depuração </span> </p> </td> 
  <td class="stentry"> <p>Execute comandos no modo de depuração. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> conteúdo </span> </p> </td> 
  <td class="stentry"> <p>Retornar informações sobre os objetos na vinheta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>Execute comandos e retorne a imagem renderizada. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops </span> </p> </td> 
  <td class="stentry"> <p>Retorna as propriedades da vinheta especificada. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> mapa </span> </p> </td> 
  <td class="stentry"> <p>Retorna os dados do mapa de imagem incorporados na vinheta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> objeto </span> </p> </td> 
  <td class="stentry"> <p>Execute comandos e retorne a imagem renderizada mascarada para a seleção de objeto atual. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> propriedades </span> </p> </td> 
  <td class="stentry"> <p>Execute comandos e retorne propriedades da imagem de resposta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">userdata </span> </p> </td> 
  <td class="stentry"> <p>Retorna o conteúdo da <span class="codeph"> vinheta::DadosUsuário </span>. </p> </td> 
 </tr> 
</table>

A menos que seja observado de outra forma nas descrições detalhadas, o servidor retorna respostas de texto com o tipo MIME &lt;text/plain>.

`debug`

Executa os comandos especificados e retorna a imagem renderizada. Se ocorrer um erro, as informações de erro e depuração serão retornadas em vez da imagem de erro ( `attribute::ErrorImagePath`).

`contents`

Retorna uma representação XML da hierarquia de objetos na vinheta, incluindo atributos de objetos selecionados. Outros comandos na solicitação são ignorados.

`img`

Executa os comandos especificados e retorna a imagem renderizada. O formato de dados de resposta e o tipo de resposta são determinados por `fmt=`.

`imageprops`

Retorna as propriedades selecionadas do arquivo de vinheta ou da entrada de catálogo especificada no caminho do URL. Consulte [Propriedades](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) para obter uma descrição da sintaxe de resposta e do tipo MIME de resposta. Outros comandos na solicitação são ignorados. As seguintes propriedades são retornadas:

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
   <td colname="col1"> <p> <span class="codeph"> image.expiration </span> </p> </td> 
   <td colname="col2"> <p>Duplo </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> atributo::Expiration </span> ou a hora padrão de vida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>Integer </p> </td> 
   <td colname="col3"> <p>Altura total da resolução em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p>nome/descrição do perfil associado a esta vinheta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>Booleano </p> </td> 
   <td colname="col3"> <p>1 se o perfil associado estiver incorporado na vinheta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>Booleano </p> </td> 
   <td colname="col3"> <p>1 se a vinheta incorporar dados de caminho. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> atributo::Modificador </span> ou vazio se não for uma entrada de catálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td colname="col2"> <p>Enum </p> </td> 
   <td colname="col3"> <p>Tipo de pixel da imagem de resposta; pode ser "CMYK", "RGB" ou "BW" (para imagens em tons de cinza). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolução de impressão padrão em dpi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p>Data/hora de modificação (do <span class="codeph"> catálogo::TimeStamp </span> ou do arquivo de vinheta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>Integer </p> </td> 
   <td colname="col3"> <p>Largura total da resolução em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p>Nome da vinheta (string de nome do objeto de vinheta raiz). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolução máxima do objeto em <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> unidades de resolução de material </a> (normalmente pixels/polegada). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolução média do objeto em <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> unidades de resolução de material </a> (normalmente pixels/inc <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> resolução de material </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Resolução mínima do objeto em <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> resolução do material </a> unidades (normalmente pixels/polegada). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>Integer </p> </td> 
   <td colname="col3"> <p>Número da versão do arquivo de vinheta. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

Retorna os dados do mapa de imagem incluídos na vinheta. Por padrão, os dados do mapa de todos os grupos mais externos são retornados. Os dados do mapa de todos os grupos internos podem ser obtidos com

`req=map&groupLevel=-1`

Os dados do mapa não estão dimensionados para `wid=` ou `hei=` ou modificados de outra forma. O tipo MIME de resposta é `<text/xml>`.

Os dados de resposta consistem em um elemento `<map>` contendo um conjunto de elementos `<area>`, semelhante à marca HTML `<AREA>`.

Cada elemento `<area>` inclui os atributos `type=` e `coord=` padrão e um atributo `name=`, especificando o nome do grupo de vinhetas ou o caminho do nome. Vários elementos `<area>` com o mesmo nome estarão presentes se as máscaras do grupo de objetos correspondente tiverem regiões descontínuas.

Além dos atributos padrão, as vinhetas podem definir atributos adicionais, se criados. Esses atributos personalizados são definidos como atributos de grupo de objetos. Os nomes de atributos personalizados devem começar com `map` para serem incluídos nos elementos `<area>`. Por exemplo, se os atributos do grupo incluírem `map.href=http://www.scene7.com`, o elemento `<area>` correspondente incluirá `href="http://www.scene7.com"`.

Um documento XML com um elemento `<map>` vazio será retornado se a vinheta não incluir dados de mapa.

`object`

Executa os comandos especificados e retorna a imagem renderizada mascarada pela seleção de objeto residual (o grupo ou objeto selecionado com o último comando `sel=` ou `obj=` na solicitação). Normalmente é usado com um formato de imagem que suporta alfa (veja [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)). Se um formato de imagem que não suporte alfa for usado, as áreas fora da máscara ficarão pretas.

`props`

Executa os comandos especificados e retorna as propriedades da vinheta e do grupo ou objeto, em vez da imagem renderizada. Consulte [Propriedades](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) para obter uma descrição da sintaxe de resposta e do tipo MIME de resposta. A seleção padrão se aplica a menos que `obj=` ou `sel=` também seja especificado (consulte [`obj=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

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
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Cor de fundo da imagem de resposta. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p>Integer </p> </td> 
   <td> <p> Altura da imagem de resposta em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> Booleano </p> </td> 
   <td> <p>Verdadeiro se o perfil ICC estiver inserido na imagem de resposta (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Nome de atalho do perfil associado à imagem de resposta (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> Booleano </p> </td> 
   <td> <p> Verdadeiro se a imagem de resposta incluir alfa. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> Booleano </p> </td> 
   <td> <p> True se a imagem de resposta incluir dados de caminho (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Tipo de imagem de resposta, pode ser "CMYK", "RGB" ou "BW" (para imagens em tons de cinza) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> Real </p> </td> 
   <td> <p> Resolução de impressão (dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>Inteiro, booleano </p> </td> 
   <td> <p> Qualidade do JPEG e sinalizador do chroma (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Tipo MIME para a imagem de resposta (consulte <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Largura da imagem de resposta em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> String de atributos para a seleção atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Número de objetos na seleção atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Valor de recuo da seleção atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selecione <span class="codeph"> selection.attributes </span>ion.name </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Caminho do nome completo da seleção de objeto atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overlapping </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> número de objetos sobrepostos na seleção atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p>Número de objetos renderizáveis na seleção atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Número de objetos texturáveis na seleção atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Status atual de mostrar/ocultar da seleção atual. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Valor da ordem Z do primeiro objeto de sobreposição na seleção atual. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

Retorna o conteúdo de `vignette::UserData`. O servidor substitui todas as ocorrências de `'??'` em `vignette::UserData` por terminadores de linha ( `<cr><lf>`). A resposta é formatada como dados de texto com o tipo MIME de resposta definido como &lt;text/plain>.

Se o objeto especificado no caminho da URL não for resolvido para uma entrada de mapa de vinheta válida ou se `vignette::UserData` estiver vazio, a resposta conterá apenas um terminador de linha ( `CR/LF`).

Quaisquer outros comandos na string de solicitação são ignorados.

## Propriedades {#section-e44092e190ff4f6380583e8ed6ea5b0b}

Comando Solicitar. Pode ocorrer em qualquer lugar na string de solicitação.

## Padrão {#section-00c593cbf1af4364b6b78812e6b93c64}

Se o URL não incluir um caminho de imagem ou modificadores, então:

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Caso contrário, `req=img`

## Consulte também {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) , [attribute::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0), [vignette::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85), [Properties](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
