---
description: Descreve alterações novas e implementadas para a API do IPS v4.0.
solution: Experience Manager
title: Novas Adições e Alterações
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1227'
ht-degree: 0%

---


# Novas Adições e Alterações{#new-additions-and-changes}

Descreve alterações novas e implementadas para a API do IPS v4.0.

Implementação de versões de API lado a lado com WSDLs e namespaces de esquema separados.

* Versões anteriores da API: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Versão do SPS 4.0: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Adição do campo `PostScriptOptions/alpha`.

Adição das propriedades `VideoRootUrl` e `SwfRootUrl` para a operação `getProperty`.

Adição dos parâmetros `appName` e `appVersion` opcionais a `authHeader` para rastrear o aplicativo de chamada. Adicionado o registro em `ipsApiService.log`.

Adição de um parâmetro `serviceUrl` opcional ao servlet de geração de WSDL. Isso é particularmente útil para depurar proxies. Por exemplo: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Operação `getZipEntries` implementada.

Intervalos de pesquisa implementados e valores de comparação digitados para condições de campo do sistema.

Adição da constante de string do tipo de ativo `'Asset'` , principalmente para permitir campos de metadados de ativos cruzados.

Implementado o parâmetro `trashState` para `searchAssets`.

Operação `getAssetPublishHistory` implementada.

Adição do cabeçalho `faultHttpStatusCode` SOAP opcional para ativar o tratamento de falhas no Flex. Para Flex, use `<faultHttpStatusCode>200</faultHttpStatusCode>`. O código de status padrão para respostas de falha é `500 (Internal Server Error)`.

Operações adicionadas para restaurar ativos da lixeira e ativos vazios da lixeira.

Operações CRUD implementadas.

Adição do sinalizador ativado ao tipo `ImageMap` e operação `saveImageMap`.

Adição de suporte para Otimizar tarefas de Arquivos Restantes.

Adição de `setAssetsPublishState` para atualizações de estado de publicação em massa.

Adição de `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Operação `saveMetadataField` obsoleta em favor de novas operações `createMetadataField` e `updateMetadataField`.

Operação de exclusão em lote `deleteAssetsParam` implementada.

Operação de movimentação em lote `moveAssetsParam` implementada.

Operação `deleteMetadataField` implementada.

Implementação de `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` operações.

Implementado `getAssetCounts`.

Adição de suporte a `setImageSetMembers` para incluir `RenderSet` membros em `ImageSet` ativos.

Adição da operação `replaceImage`.

Adição da operação `copyImage`.

Adição da operação `setUrlModifier` e dos campos `urlModifier/urlPostApplyModifier` para `LayerViewInfo`, `TemplateInfo` e `WatermarkInfo`.

Adição da operação `createDerivedAsset`. Atualmente, `ownerHandle` deve fazer referência a um ativo de Imagem e o tipo pode ser `AdjustedView` ou `LayerView`.

Adição da operação `createTemplate`. Atualmente, isso pode ser chamado para criar ativos de Modelo ou Marca d&#39;água.

Configurações da empresa IPS, `CompanySettings`, portadas para a API de serviços da Web.

Adição do sinalizador de filtro `excludeByproducts` à operação `searchAssets`. Configurar esse sinalizador como true executa `PSDlayer` imagens e imagens rasgadas em PDF.

Adição da operação `getGenerationInfo`.

Adição do nome da propriedade `SystemMessage` à operação `getProperty`.

Foram modificadas algumas constantes da cadeia de caracteres do tipo de ativo para corresponderem aos campos de Informações do ativo correspondentes.

* WordDoc: Palavra
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Formato de resultado modificado de operações em lote para resumir erros, avisos e sucesso.

Implementação de `batchSetAssetMetadata` metadados em lote.

Suporte implementado para dados específicos do aplicativo.

Implementação de suporte para sinalizadores booleanos para `createTemplate`, `extendLayers` e `extractText` para trabalhos de upload para controlar o processo de processamento do Photoshop (semelhante às alterações para adicionar uploads de arquivo).

Implementação de `setImageMaps` e `setZoomTargets` operações.

Implementação de `ViewerPreset` operações. Os tipos reconhecidos são:

* `VideoPlayer` (O vídeo só publica esses visualizadores.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

As capas do visualizador suportam dois parâmetros: `skinFg` e `skinBg`. O código de backend executará todo o processamento necessário para manter a compatibilidade com versões anteriores.

Operação `getAssociatedAssets` implementada.

Adição do tipo de trabalho `ReprocessAssets` para permitir o reprocessamento de arquivos de origem primária carregados anteriormente, incluindo a repetição de PDFs e a reotimização de imagens.

Tipo de campo `PropertySetType` renomeado para `propertyType`. Isso afeta o parâmetro `createPropertySetType` e a resposta `getPropertySetType/getPropertySetTypes`.

Implementação da operação `batchSetImageFields` para oferecer suporte à configuração de dados do usuário da imagem e outros campos de imagem editáveis.

47 Adição do campo fileSize a vários tipos de informações de ativos:

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

Operação `getActivePublishContexts` implementada. Essa operação retorna uma matriz de nomes de contexto de publicação com servidores de publicação ativos para a empresa especificada. Os nomes de contexto de publicação atuais são:

* `ImageServing`
* `ImageRendering`
* `Video`

Operação `getSearchStrings` implementada. Retorna uma matriz de sequências de pesquisa para o ativo em questão.

Adição de parâmetros de localidade para tarefas e um mecanismo para definir a localidade para operações de API. A cadeia de caracteres de localidade deve ser formatada como `<language_code>[-<country_code>]`. O código de idioma é um código de duas letras minúsculo, conforme especificado pela ISO-639, e o código opcional de país é um código de duas letras maiúsculas, conforme especificado pela ISO-3166.

Adição do parâmetro de localidade opcional ao cabeçalho SOAP `authHeader` para definir a localidade para operações de API. Se esse parâmetro não estiver presente, o cabeçalho HTTP `Accept-Language` será usado. Se esse cabeçalho também não estiver presente, a localidade padrão do servidor IPS será usada.

Adição do suporte a get/set para campos de metadados altamente digitados.

Implementação de suporte a SOAP e cabeçalho HTTP para controle de resposta gzip.

Adição do sinalizador `gzipResponse` a `authHeader`. Se não estiver presente, a API também verificará o cabeçalho HTTP `Accept-Encoding`.

Adição de suporte ao searchAssets para obter condições de campo de metadados altamente digitadas.

* Para todos os tipos de campo, o valor pode ser passado com um operador de comparação de cadeia de caracteres ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Para campos booleanos, `boolVal` pode ser passado com a parte superior `Equals`.
* Para campos Int , `longVal` pode ser transmitido com um operador de comparação numérico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou `minLong/maxLong` pode ser passado com operações de intervalo numérico ( `Between, NotBetween`).
* Para campos Flutuantes, `doubleVal` pode ser passado com um operador de comparação numérico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou `minDouble/maxDouble` pode ser passado com operações de intervalo numérico ( `Between, NotBetween`).
* Para campos de Data , você pode passar `dateVal` com um operador de comparação numérica ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou pode passar minDate/maxDate com uma operação de intervalo numérico ( `Between, NotBetween`).

Adicionados descrição, campos `jobSubType` e `originalJobName` ao tipo `JobLog`.

* `originalJobName` é o nome do cargo enviado para  `submitJob` (sem sufixos exclusivos ou nomes de tarefas complementares).
* `jobSubType` é atualmente usada apenas por  `ImageServingPublishJob` trabalhos (onde é um de  `full`,  `increment, fullwithsearch,` ou  `fulloverride`).
* `description` no momento, é uma string vazia para todos os tipos de tarefas, mas eventualmente conterá informações de trabalhos de resumo, como o caminho de upload.

Além disso, os seguintes campos não estão incluídos com `getJobLogs` e `getJobLogDetails`. Em versões anteriores, eles só estavam disponíveis com `getJobLogDetails`.

* `endDate` (se o trabalho tiver sido concluído).
* `fileDuplicateCount` (anteriormente, sempre estava  `0` com  `getJobLogs`)
* `fileUpdateCount` (anteriormente era sempre  `0` com  `getJobLogs` e incluído em  `fileSuccessCount`; agora é dividido em campos separados).

Adição do campo assetHandle ao tipo `JobLogDetail` .

Adição do parâmetro de descrição opcional para `submitJob`. Isso é passado para recuperação em `getScheduledJobs`, `getActiveJobs` e `getJobLogs`.

Campo do sistema SKU descontinuado. O campo será ignorado se for passado como um `SystemFieldCondition` para `searchAssets`.

Adição do filtro `excludeAssetTypeArray` a `searchAssets`.

Adição do tipo `MaskInfo` a `Asset`.

Adicionados novos Tipos de ativos para gerenciamento por IPS:

<table id="table_DCCE936B797A448598C30E3B344525A5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tipo de ativo </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Illustrator  </span> </p> </td> 
   <td colname="col2"> <p>Arquivo Adobe Illustrator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript  </span> </p> </td> 
   <td colname="col2"> <p>Arquivos EPS e PostScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc  </span> </p> </td> 
   <td colname="col2"> <p>Documento do Microsoft Word para arquivos terminados com .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc  </span> </p> </td> 
   <td colname="col2"> <p>Documento do Microsoft Excel para arquivos que terminam com .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc  </span> </p> </td> 
   <td colname="col2"> <p>Documento do Microsoft PowerPoint para arquivos terminados com .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc  </span> </p> </td> 
   <td colname="col2"> <p>Arquivo RTF para arquivos carregados terminando com .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Adicionadas opções adicionais para `UploadDirectoryJob` e `UploadUrlsJob` para controlar o processamento de arquivos Postscript, Illustrator e PDF de maneira independente. Todas as tarefas existentes fornecerão os parâmetros necessários para cada um dos três pipelines de processamento para que funcionem exatamente como é feito hoje. O bloco original `PostScriptOptions` é usado para definir o processamento para arquivos Illustrator e EPS/PS. Opcionalmente, blocos de opções de arquivo específicos podem ser fornecidos para especificar o processamento. A lista de alterações inclui:

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo  </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Nenhum  </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rasterizar  </span>(padrão) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Gerenciar somente o ativo e não criar derivados ao fazer upload. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Renderize o arquivo EPS e PostScript em uma imagem na resolução e no espaço de cores prescritas. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa  </span> </p> <p>Opcional. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Tem efeito ao rasterizar o arquivo em uma imagem. Ele criará um fundo transparente se o arquivo original for definido dessa forma para sobreposição de logotipos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo  </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Nenhum  </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rasterizar  </span> (padrão) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Gerenciar somente o ativo e não criar derivados ao fazer upload. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Renderize o arquivo em uma imagem na resolução e no espaço de cores prescritas. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterizando resolução. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> colorspace  </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espaço de cores de destino para renderização. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa  </span> </p> <p>Opcional. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Tem efeito ao rasterizar o arquivo em uma imagem. Cria um fundo transparente se o arquivo original estiver definido dessa forma para a criação de logotipos sobrepostos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOoptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo  </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Nenhum  </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rasterizar  </span> (padrão) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Gerenciar somente o ativo e não criar derivados ao fazer upload. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Renderize o arquivo em uma imagem na resolução e no espaço de cores prescritas. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterizando resolução. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> colorspace  </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espaço de cores de destino para renderização. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define se um PDF de várias páginas deve ser combinado em um eCatalog após a renderização (o padrão é verdadeiro). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define se as palavras do PDF são extraídas no banco de dados para serem fornecidas posteriormente a um servidor de pesquisa (o padrão é false). </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> never  </span> </p> </td> 
   <td colname="col2"> <p>Não responda ao gzip. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sabão  </span> </p> </td> 
   <td colname="col2"> <p>Resposta de gzip somente se authHeader/gzipResponse for verdadeiro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> accept  </span> </p> </td> 
   <td colname="col2"> <p>Gzip se authHeader/gzipResponse for true ou se nenhum cabeçalho gzipResponse estiver presente e o cabeçalho HTTP Accept-Encoding incluir gzip. (Padrão). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always  </span> </p> </td> 
   <td colname="col2"> <p>Sempre gzip de resposta, independentemente dos valores do cabeçalho. Use esse valor somente para fins de depuração. </p> </td> 
  </tr> 
 </tbody> 
</table>

