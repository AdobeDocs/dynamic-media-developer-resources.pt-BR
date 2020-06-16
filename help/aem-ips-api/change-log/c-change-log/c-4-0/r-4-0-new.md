---
description: Descreve alterações novas e implementadas para a API IPS v4.0.
seo-description: Descreve alterações novas e implementadas para a API IPS v4.0.
seo-title: Novas Adições e Alterações
solution: Experience Manager
title: Novas Adições e Alterações
topic: Scene7 Image Production System API
uuid: ca4bbe36-c1b7-471f-90a8-6b695d56ac7a
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '1234'
ht-degree: 0%

---


# Novas Adições e Alterações{#new-additions-and-changes}

Descreve alterações novas e implementadas para a API IPS v4.0.

Implementadas versões de API lado a lado com WSDLs e namespaces schemas separadas.

* Versões anteriores da API: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Versão do SPS 4.0: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Campo adicionado `PostScriptOptions/alpha` .

Propriedades adicionadas `VideoRootUrl` e `SwfRootUrl` para `getProperty` operação.

Adicionados parâmetros opcionais `appName` e `appVersion` opcionais `authHeader` para rastrear o aplicativo de chamada. Adicionado o registro em `ipsApiService.log`.

Foi adicionado um `serviceUrl` parâmetro opcional ao servlet de geração WSDL. Isso é particularmente útil para depurar proxies. Por exemplo: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Operação `getZipEntries` implementada.

Intervalos de pesquisa implementados e valores de comparação digitados para condições de campo do sistema.

Adicionada uma constante de string de tipo de ativo, principalmente para permitir campos de metadados entre ativos. `'Asset'`

Param implementado `trashState` para `searchAssets`.

Operação `getAssetPublishHistory` implementada.

Adicionado um cabeçalho `faultHttpStatusCode` SOAP opcional para ativar a manipulação de falhas no Flex. Para Flex, use `<faultHttpStatusCode>200</faultHttpStatusCode>`. O código de status padrão para respostas de falha é `500 (Internal Server Error)`.

Foram adicionadas operações para restaurar ativos do lixo e ativos vazios do lixo.

Operações CRUD implementadas.

Sinalizador ativado adicionado para `ImageMap` digitar e `saveImageMap` operação.

Adicionado suporte para Otimizar trabalhos de Arquivos Restantes.

Adicionado `setAssetsPublishState` para atualizações de estado de publicação em massa.

Adicionado `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Operação obsoleta em favor de novas `saveMetadataField` e `createMetadataField` `updateMetadataField` operações.

Operação de exclusão de `deleteAssetsParam` lote implementada.

Operação `moveAssetsParam` de movimentação em lote implementada.

Operação `deleteMetadataField` implementada.

Implementado `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` operações.

Implementado `getAssetCounts`.

Adição de suporte `setImageSetMembers` para inclusão `RenderSet` de membros em `ImageSet` ativos.

Operação adicionada. `replaceImage`

Operação adicionada. `copyImage`

Operação `setUrlModifier` e `urlModifier/urlPostApplyModifier` campos adicionados para `LayerViewInfo`, `TemplateInfo`e `WatermarkInfo`.

Operação adicionada. `createDerivedAsset` Atualmente, o `ownerHandle` deve fazer referência a um ativo de Imagem e o tipo pode ser `AdjustedView` ou `LayerView`.

Operação adicionada. `createTemplate` Atualmente, isso pode ser chamado para criar ativos de Modelo ou Marca d&#39;água.

Configurações de empresa IPS, `CompanySettings`, portadas para a API de serviços da Web.

Sinalizador `excludeByproducts` de filtro adicionado à `searchAssets` operação. Configurar esse sinalizador para verdadeiro executa `PSDlayer` imagens e imagens rasgadas de PDF.

Operação adicionada. `getGenerationInfo`

Nome `SystemMessage` da propriedade adicionado à `getProperty` operação.

Foram modificadas algumas constantes de string de tipo de ativo para corresponder aos campos de Informações do ativo correspondentes.

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Formato de resultado modificado de operações em lote para resumir o sucesso, os avisos e os erros.

Operação de metadados `batchSetAssetMetadata` em lote implementada.

Suporte implementado para dados específicos do aplicativo.

Suporte implementado para sinalizadores booleanos para `createTemplate`, `extendLayers`e `extractText` para trabalhos de upload para controlar o processo de processamento do Photoshop (semelhante a alterações para uploads de arquivos adicionados).

Executado `setImageMaps` e `setZoomTargets` operacoes.

Operações `ViewerPreset` executadas. Os tipos reconhecidos são:

* `VideoPlayer` (O vídeo só publica esses visualizadores.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

As capas do visualizador suportam dois parâmetros: `skinFg` e `skinBg`. O código backend executará todo o processamento necessário para manter a compatibilidade com versões anteriores.

Operação `getAssociatedAssets` implementada.

Adicionado o tipo de `ReprocessAssets` trabalho para permitir o reprocessamento de arquivos de origem primária carregados anteriormente, incluindo a repetição de PDFs e a reotimização de imagens.

Tipo de `PropertySetType` campo renomeado para `propertyType`. Isso afeta o `createPropertySetType` parâmetro e a `getPropertySetType/getPropertySetTypes` resposta.

Operação implementada `batchSetImageFields` para suportar a configuração de dados do usuário da imagem e outros campos de imagem editáveis.

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

Operação `getActivePublishContexts` implementada. Esta operação retorna uma matriz de nomes de contexto de publicação com servidores de publicação ativos para a empresa especificada. Os nomes de contexto de publicação atuais são:

* `ImageServing`
* `ImageRendering`
* `Video`

Operação `getSearchStrings` implementada. Ele retorna uma matriz de sequências de pesquisa para o ativo em questão.

Foram adicionados parâmetros de localidade para trabalhos e um mecanismo para definir a localidade para operações de API. A sequência de caracteres de localidade deve ser formatada como `<language_code>[-<country_code>]`. O código de idioma é um código de duas letras minúsculas, conforme especificado pela ISO-639, e o código de país opcional é um código de duas letras maiúsculas, conforme especificado pela ISO-3166.

Foi adicionado um parâmetro de localidade opcional ao cabeçalho `authHeader` SOAP para definir a localidade para operações de API. Se esse parâmetro não estiver presente, o cabeçalho HTTP `Accept-Language` será usado. Se esse cabeçalho também não estiver presente, a localidade padrão do servidor IPS será usada.

Adição do suporte a get/set para campos de metadados digitados fortemente.

Suporte a SOAP e cabeçalho HTTP implementado para controle de resposta gzip.

Sinalizador adicionado `gzipResponse` ao `authHeader`. Se não estiver presente, a API também verificará o cabeçalho HTTP `Accept-Encoding` .

Adição de suporte ao SearchAssets para condições de campo de metadados digitados fortemente.

* Para todos os tipos de campo, o valor pode ser transmitido com um operador de comparação de string ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Para campos booleanos, `boolVal` pode ser passado com o `Equals` op.
* Para campos Int, `longVal` pode ser transmitido com um operador de comparação numérica ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou `minLong/maxLong` pode ser transmitido com uma operação de intervalo numérico ( `Between, NotBetween`).
* Para campos flutuantes, `doubleVal` pode ser passado com um operador de comparação numérica ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou `minDouble/maxDouble` pode ser passado com uma operação de intervalo numérico ( `Between, NotBetween`).
* Para campos de Data, você pode passar `dateVal` com um operador de comparação numérica ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou pode passar minDate/maxDate com uma operação de intervalo numérico ( `Between, NotBetween`).

Descrição, `jobSubType`e `originalJobName` campos adicionados para `JobLog` digitar.

* `originalJobName` é o nome do serviço enviado `submitJob` (sem sufixos de exclusividade ou nomes de trabalhos de continuação).
* `jobSubType` atualmente é usado apenas por `ImageServingPublishJob` trabalhos (onde é um `full`, `increment, fullwithsearch,` ou `fulloverride`).
* `description` no momento, é uma string vazia para todos os tipos de trabalho, mas eventualmente conterá informações de trabalho resumidas, como o caminho de upload.

Além disso, os campos a seguir não são incluídos tanto `getJobLogs` quanto `getJobLogDetails`. Em versões anteriores, eles só estavam disponíveis com `getJobLogDetails`.

* `endDate` (se o trabalho tiver sido concluído).
* `fileDuplicateCount` (antes, sempre estava `0` com `getJobLogs`)
* `fileUpdateCount` (anteriormente, estava sempre `0` com `getJobLogs` e incluído em `fileSuccessCount`; agora é dividido em campos separados).

Adição do campo assetHandle ao `JobLogDetail` tipo.

Foi adicionado um parâmetro de descrição opcional ao `submitJob`. Isso é passado para recuperação em `getScheduledJobs`, `getActiveJobs`e `getJobLogs`.

Campo do sistema SKU substituído. O campo será ignorado se for passado como um `SystemFieldCondition` para `searchAssets`.

Adicionado `excludeAssetTypeArray` o filtro ao `searchAssets`.

Adicionado `MaskInfo` o tipo ao `Asset`.

Adicionados novos tipos de ativos para gerenciamento pelo IPS:

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
   <td colname="col2"> <p>Arquivo do Adobe Illustrator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>Arquivos EPS e PostScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>documento do Microsoft Word para arquivos que terminam com .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>documento do Microsoft Excel para arquivos que terminam com .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>documento do Microsoft PowerPoint para arquivos que terminam com .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>Arquivo RTF para arquivos carregados terminando com .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Adicionadas outras opções para `UploadDirectoryJob` e para controlar `UploadUrlsJob` o processamento de arquivos Postscript, Illustrator e PDF de forma independente. Todos os trabalhos existentes fornecerão os parâmetros necessários para cada um dos três pipelines de processamento, para que funcionem exatamente como acontece hoje. O `PostScriptOptions` bloco original é usado para definir o processamento para arquivos Illustrator e EPS/PS. Como opção, blocos de opções de arquivo específicos podem ser fornecidos para especificar o processamento. A lista de alterações inclui:

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Nenhum </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rasterizar </span>(padrão) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Gerenciar somente o ativo e não criar nenhum derivado após o upload. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Renderize o arquivo EPS e PostScript em uma imagem na resolução e no espaço de cores prescritas. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Opcional. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Tem efeito ao rasterizar o arquivo em uma imagem. Isso criará um fundo transparente se o arquivo original for definido dessa forma para a sobreposição de logotipos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Nenhum </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rasterizar </span> (padrão) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Gerenciar somente o ativo e não criar nenhum derivado após o upload. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Renderize o arquivo em uma imagem com a resolução e o espaço de cor prescritos. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolução </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterizando resolução. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> colorspace </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espaço de cor do Público alvo para renderização. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Opcional. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>É afetado ao rasterizar o arquivo em uma imagem. Cria um fundo transparente se o arquivo original for definido dessa forma para a criação de logotipos sobrepostos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOoptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Nenhum </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rasterizar </span> (padrão) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Gerenciar somente o ativo e não criar nenhum derivado após o upload. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Renderize o arquivo em uma imagem com a resolução e o espaço de cor prescritos. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolução </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterizando resolução. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> colorspace </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espaço de cor do Público alvo para renderização. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define se um PDF de várias páginas deve ser combinado em um eCatalog após a renderização (o padrão é true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define se as palavras do PDF são extraídas no DB para posterior fornecimento a um servidor de pesquisa (o padrão é false). </p> </td> 
  </tr> 
 </tbody> 
</table>

Você também pode query de `getScheduledJobs`.

Modificada a propriedade `webservice.gzip.response` configuration para obter um dos seguintes valores:

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valor </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nunca </span> </p> </td> 
   <td colname="col2"> <p>Não responda ao gzip. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sabão </span> </p> </td> 
   <td colname="col2"> <p>Resposta de gzip somente se authHeader/gzipResponse for verdadeiro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> accept </span> </p> </td> 
   <td colname="col2"> <p>Gzip se authHeader/gzipResponse for verdadeiro ou se nenhum cabeçalho gzipResponse estiver presente e o cabeçalho HTTP Accept-Encoding incluir gzip. (Padrão). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always </span> </p> </td> 
   <td colname="col2"> <p>Sempre obtenha resposta, independentemente dos valores do cabeçalho. Use esse valor somente para fins de depuração. </p> </td> 
  </tr> 
 </tbody> 
</table>

