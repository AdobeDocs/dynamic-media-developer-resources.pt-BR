---
title: Novas Adições e Alterações
description: Descreve as alterações novas e implementadas para a API do IPS v4.0.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 0%

---

# Novas Adições e Alterações{#new-additions-and-changes}

Descreve as alterações novas e implementadas para a API do IPS v4.0.

Versões da API lado a lado implementadas com WSDLs e namespaces de esquema separados.

* Versões anteriores da API: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Versão do SPS 4.0: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Adição do campo `PostScriptOptions/alpha`.

Adicionadas as propriedades `VideoRootUrl` e `SwfRootUrl` da operação `getProperty`.

Adicionados parâmetros `appName` e `appVersion` opcionais a `authHeader` para rastrear o aplicativo de chamada. Adição de log a `ipsApiService.log`.

Adição de um parâmetro `serviceUrl` opcional ao servlet de geração WSDL. Esse parâmetro é útil para proxies de depuração. Por exemplo: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Implementou a operação `getZipEntries`.

Intervalos de pesquisa implementados e valores de comparação digitados para condições de campo do sistema.

Adição da constante de cadeia de caracteres de tipo de ativo `'Asset'`, principalmente para permitir campos de metadados entre ativos.

Implementou o parâmetro `trashState` para `searchAssets`.

Implementou a operação `getAssetPublishHistory`.

Adição do cabeçalho `faultHttpStatusCode` SOAP opcional para habilitar o tratamento de falhas no Flex. Para Flex, use `<faultHttpStatusCode>200</faultHttpStatusCode>`. O código de status padrão para respostas de falha é `500 (Internal Server Error)`.

Adição de operações para restaurar ativos da lixeira e esvaziar ativos da lixeira.

Operações CRUD implementadas.

Adição do sinalizador habilitado ao tipo `ImageMap` e operação `saveImageMap`.

Adição de suporte para os trabalhos Otimizar arquivos restantes.

Adicionado `setAssetsPublishState` para atualizações de estado de publicação em massa.

Adicionado `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Operação `saveMetadataField` descontinuada em favor de novas operações `createMetadataField` e `updateMetadataField`.

Implementou a operação de exclusão em lote `deleteAssetsParam`.

Implementou a operação de movimentação em lote `moveAssetsParam`.

Implementou a operação `deleteMetadataField`.

Implementou `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` operações.

Implementado `getAssetCounts`.

Adicionado suporte a `setImageSetMembers` para inclusão de `RenderSet` membros em `ImageSet` ativos.

Adicionada a operação `replaceImage`.

Adicionada a operação `copyImage`.

Adicionada a operação `setUrlModifier` e os campos `urlModifier/urlPostApplyModifier` para `LayerViewInfo`, `TemplateInfo` e `WatermarkInfo`.

Adicionada a operação `createDerivedAsset`. Atualmente, o `ownerHandle` deve fazer referência a um ativo de imagem e o tipo pode ser `AdjustedView` ou `LayerView`.

Adicionada a operação `createTemplate`. Chamada para criar ativos de Modelo ou Marca d&#39;água.

Configurações da empresa de IPS, `CompanySettings`, transferidas para a API de serviços da Web.

Adicionado o sinalizador de filtro `excludeByproducts` à operação `searchAssets`. Configurar este sinalizador como true executa `PSDlayer` imagens e imagens extraídas do PDF.

Adicionada a operação `getGenerationInfo`.

Adição do nome da propriedade `SystemMessage` à operação `getProperty`.

Foram modificadas algumas constantes da sequência de caracteres do tipo de ativo para corresponder aos campos de Informações do ativo correspondentes.

* WordDoc: palavra
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Formato de resultado modificado de operações em lote para resumir êxito, avisos e erros.

Implementou a operação de metadados em lote `batchSetAssetMetadata`.

Implementação de suporte para dados específicos do aplicativo.

Implementação de suporte para sinalizadores booleanos para `createTemplate`, `extendLayers` e `extractText` para trabalhos de carregamento para controlar o processo de processamento do Photoshop (semelhante a alterações para adicionar carregamentos de arquivo).

Implementou `setImageMaps` e `setZoomTargets` operações.

`ViewerPreset` operações implementadas. Os tipos reconhecidos são:

* `VideoPlayer` (O vídeo só publica esses visualizadores.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

As capas do visualizador dão suporte a dois parâmetros: `skinFg` e `skinBg`. O código de backend faz todo o processamento necessário para manter a compatibilidade com versões anteriores.

Implementou a operação `getAssociatedAssets`.

Adição do tipo de trabalho `ReprocessAssets` para permitir o reprocessamento de arquivos de origem primários carregados anteriormente, incluindo a cópia de PDFs e a reotimização de imagens.

Tipo de campo `PropertySetType` renomeado para `propertyType`. Essa renomeação afeta o parâmetro `createPropertySetType` e a resposta `getPropertySetType/getPropertySetTypes`.

Implementação da operação `batchSetImageFields` para oferecer suporte à configuração de dados de usuário de imagem e outros campos de imagem editáveis.

47 Adição do campo fileSize a vários tipos de informações do ativo:

* `VignetteInfo`
* `CabinetInfo`
* `WindowCoveringInfo`
* `IccProfileInfo`
* `FontInfo`
* `XslInfo`
* `ViewerSwfInfo`
* `XmlInfo`
* `SvgInfo`
* `ZipInfo`
* `VideoInfo`
* `AcoInfo`
* `PdfInfo`
* `PsdInfo`
* `FlashInfo`
* `InDesignInfo`
* `PostScriptInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `RTFInfo`

Implementou a operação `getActivePublishContexts`. Esta operação retorna uma matriz de nomes de contexto de publicação com servidores de publicação ativos para a empresa especificada. Os nomes do contexto de publicação atual são:

* `ImageServing`
* `ImageRendering`
* `Video`

Implementou a operação `getSearchStrings`. Ele retorna uma matriz de sequências de caracteres de pesquisa para o ativo fornecido.

Adição de parâmetros de localidade para trabalhos e um mecanismo para definir a localidade para operações de API. A cadeia de caracteres local deve ser formatada como `<language_code>[-<country_code>]`. O código de idioma é um código de duas letras em minúsculas, conforme especificado pela ISO-639, e o código opcional de país é um código de duas letras em maiúsculas, conforme especificado pela ISO-3166.

Adição do parâmetro de localidade opcional ao cabeçalho do SOAP `authHeader` para definir a localidade das operações da API. Se este parâmetro não estiver presente, o cabeçalho HTTP `Accept-Language` será usado. Se esse cabeçalho também não estiver presente, o local padrão do servidor IPS será usado.

Adição de suporte get/set para campos de metadados fortemente tipados.

Implementação de suporte a cabeçalho SOAP e HTTP para controle de resposta gzip.

Adicionou o sinalizador `gzipResponse` a `authHeader`. Se não estiver presente, a API verificará o cabeçalho HTTP `Accept-Encoding`.

Adição de suporte a searchAssets para condições de campo de metadados fortemente tipados.

* Para todos os tipos de campo, o valor pode ser passado com um operador de comparação de sequência ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Para campos booleanos, `boolVal` pode ser passado com a `Equals` op.
* Para campos Int, `longVal` pode ser passado com um operador de comparação numérica ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou `minLong/maxLong` pode ser passado com operações de intervalo numérico ( `Between, NotBetween`).
* Para campos flutuantes, `doubleVal` pode ser passado com um operador de comparação numérica ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou `minDouble/maxDouble` pode ser passado com operações de intervalo numérico ( `Between, NotBetween`).
* Para campos de Data, você pode passar `dateVal` com um operador de comparação numérica ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou minDate/maxDate com operações de intervalo numérico ( `Between, NotBetween`).

Adição dos campos descrição, `jobSubType` e `originalJobName` ao tipo `JobLog`.

* `originalJobName` é o nome do trabalho enviado a `submitJob` (sem nenhum sufixo de exclusividade ou nome de trabalho de acompanhamento).
* `jobSubType` é usado somente por `ImageServingPublishJob` trabalhos (em que é um de `full`, `increment, fullwithsearch,` ou `fulloverride`).
* `description` é uma cadeia de caracteres vazia para todos os tipos de trabalho, mas eventualmente contém informações resumidas do trabalho, como o caminho de carregamento.

Além disso, os campos a seguir não estão incluídos com `getJobLogs` e `getJobLogDetails`. Em versões anteriores, eles só estavam disponíveis com `getJobLogDetails`.

* `endDate` (se o trabalho foi concluído).
* `fileDuplicateCount` (anteriormente era sempre `0` com `getJobLogs`)
* `fileUpdateCount` (anteriormente era sempre `0` com `getJobLogs` e incluído em `fileSuccessCount`; agora está dividido em campos separados).

Adição do campo assetHandle ao tipo `JobLogDetail`.

Adição do parâmetro de descrição opcional a `submitJob`. Este parâmetro é passado para recuperação em `getScheduledJobs`, `getActiveJobs` e `getJobLogs`.

O campo do sistema SKU foi descontinuado. O campo será ignorado se for passado como `SystemFieldCondition` para `searchAssets`.

Adicionado o filtro `excludeAssetTypeArray` a `searchAssets`.

Adição do tipo `MaskInfo` a `Asset`.

Adição de novos Tipos de ativos para gerenciamento por IPS:

<table id="table_DCCE936B797A448598C30E3B344525A5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tipo de ativo </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Illustrator </span> </p> </td> 
   <td colname="col2"> <p>arquivo Adobe Illustrator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>Arquivos EPS e PostScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>Documento do Microsoft® Word para arquivos terminados com .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>Documento do Microsoft® Excel para arquivos terminados com .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>Documento do Microsoft® PowerPoint para arquivos terminados com .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>Arquivo RTF para arquivos carregados terminando com .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Adicionadas opções adicionais a `UploadDirectoryJob` e `UploadUrlsJob` para controlar o processamento de arquivos Postscript, Illustrator e PDF independentemente. Todas as tarefas existentes fornecem os parâmetros necessários para cada um dos três pipelines de processamento, para que funcionem exatamente como hoje. O bloco `PostScriptOptions` original é usado para definir o processamento de arquivos Illustrator e EPS/PS. Opcionalmente, blocos de opções de arquivo específicos podem ser fornecidos para especificar o processamento. A lista de alterações inclui:

<table id="table_D4E5ACCB2D144D05A5FA0129AA5F9344"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Campo </p> </th> 
   <th colname="col2" class="entry"> <p>Parâmetro </p> </th> 
   <th colname="col3" class="entry"> <p>Valor </p> </th> 
   <th colname="col4" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p> <span class="codeph"> [!DNL PostScriptOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL process] </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Nenhum </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rasterizar </span> (padrão) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Gerencie somente o ativo e não crie derivados após o upload. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Renderize o arquivo EPS e PostScript em uma imagem com a resolução e o espaço de cor prescritos. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Opcional. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;booleano&gt; </span> </p> </td> 
   <td colname="col4"> <p>Tem efeito ao rasterizar o arquivo em uma imagem. Ele cria um plano de fundo transparente se o arquivo original for definido dessa maneira para sobrepor logotipos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Nenhum </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rasterizar </span> (padrão) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Gerencie somente o ativo e não crie derivados após o upload. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Renderize o arquivo em uma imagem com a resolução e o espaço de cor prescritos. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;inteiro&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterizando a resolução. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espaço de cor de destino para renderização. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Opcional. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Tem efeito ao rasterizar o arquivo em uma imagem. Cria um plano de fundo transparente se o arquivo original for definido dessa maneira para criar logotipos de sobreposição. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Nenhum </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rasterizar </span> (padrão) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Gerencie somente o ativo e não crie derivados após o upload. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Renderize o arquivo em uma imagem com a resolução e o espaço de cor prescritos. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;inteiro&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterizando a resolução. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espaço de cor de destino para renderização. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;booleano&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define se um PDF de várias páginas deve ser combinado em um eCatalog após a renderização (o padrão é verdadeiro). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;booleano&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define se as palavras do PDF são extraídas no banco de dados para fornecimento posterior a um servidor de pesquisa (o padrão é falso). </p> </td> 
  </tr> 
 </tbody> 
</table>

Você também pode consultar de `getScheduledJobs`.

A propriedade de configuração `webservice.gzip.response` foi modificada para assumir um dos seguintes valores:

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valor </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL never] </span> </p> </td> 
   <td colname="col2"> <p>Não use gzip na resposta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>A resposta do Gzip somente se authHeader/gzipResponse for verdadeira. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>Gzip se authHeader/gzipResponse for true, ou se nenhum cabeçalho gzipResponse estiver presente e o cabeçalho HTTP Accept-Encoding incluir gzip. (Padrão). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>Sempre dê uma resposta com gzip, independentemente dos valores do cabeçalho. Use esse valor somente para fins de depuração. </p> </td> 
  </tr> 
 </tbody> 
</table>
