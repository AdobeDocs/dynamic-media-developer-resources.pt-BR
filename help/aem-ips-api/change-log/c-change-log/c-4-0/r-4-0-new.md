---
title: Novas Adições e Alterações
description: Descreve as alterações novas e implementadas para a API do IPS v4.0.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---

# Novas Adições e Alterações{#new-additions-and-changes}

Descreve as alterações novas e implementadas para a API do IPS v4.0.

Versões da API lado a lado implementadas com WSDLs e namespaces de esquema separados.

* Versões anteriores da API: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Versão do SPS 4.0: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Adicionado `PostScriptOptions/alpha` campo.

Adicionado `VideoRootUrl` e `SwfRootUrl` propriedades para `getProperty` operação.

Adição de opcional `appName` e `appVersion` parâmetros para `authHeader` para rastrear o aplicativo de chamada. Adição de logon no `ipsApiService.log`.

Adição de um opcional `serviceUrl` para o servlet de geração WSDL. Esse parâmetro é útil para proxies de depuração. Por exemplo: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Implementado `getZipEntries` operação.

Intervalos de pesquisa implementados e valores de comparação digitados para condições de campo do sistema.

Adicionado `'Asset'` constante de sequência de caracteres do tipo de ativo, principalmente para permitir campos de metadados entre ativos.

Implementado `trashState` parâmetro para `searchAssets`.

Implementado `getAssetPublishHistory` operação.

Adição de opcional `faultHttpStatusCode` Cabeçalho SOAP para habilitar o manuseio de falhas no Flex. Para o Flex, use `<faultHttpStatusCode>200</faultHttpStatusCode>`. O código de status padrão para respostas de falha é `500 (Internal Server Error)`.

Adição de operações para restaurar ativos da lixeira e esvaziar ativos da lixeira.

Operações CRUD implementadas.

Adicionado sinalizador ativado a `ImageMap` tipo e `saveImageMap` operação.

Adição de suporte para os trabalhos Otimizar arquivos restantes.

Adicionado `setAssetsPublishState` para atualizações de estado de publicação em massa.

Adicionado `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Obsoleto `saveMetadataField` operação a favor de novas `createMetadataField` e `updateMetadataField` operações.

Implementado `deleteAssetsParam` operação de exclusão em lote.

Implementado `moveAssetsParam` operação de movimentação de lote.

Implementado `deleteMetadataField` operação.

Implementado `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` operações.

Implementado `getAssetCounts`.

Adição de suporte ao `setImageSetMembers` para incluir `RenderSet` membros em `ImageSet` ativos.

Adicionado `replaceImage` operação.

Adicionado `copyImage` operação.

Adicionado `setUrlModifier` operação e `urlModifier/urlPostApplyModifier` campos para `LayerViewInfo`, `TemplateInfo`, e `WatermarkInfo`.

Adicionado `createDerivedAsset` operação. Atualmente, o `ownerHandle` deve fazer referência a um ativo de imagem e o tipo pode ser `AdjustedView` ou `LayerView`.

Adicionado `createTemplate` operação. Chamada para criar ativos de Modelo ou Marca d&#39;água.

Configurações da empresa IPS, `CompanySettings`, transferido para a API de serviços da Web.

Adicionado `excludeByproducts` sinalizador de filtro para `searchAssets` operação. A definição desse sinalizador como true é executada `PSDlayer` imagens e PDF copiadas.

Adicionado `getGenerationInfo` operação.

Adicionado `SystemMessage` nome da propriedade para `getProperty` operação.

Foram modificadas algumas constantes da sequência de caracteres do tipo de ativo para corresponder aos campos de Informações do ativo correspondentes.

* WordDoc: palavra
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Formato de resultado modificado de operações em lote para resumir êxito, avisos e erros.

Implementado `batchSetAssetMetadata` operação de metadados em lote.

Implementação de suporte para dados específicos do aplicativo.

Suporte implementado para sinalizadores booleanos para `createTemplate`, `extendLayers`, e `extractText` para trabalhos de upload para controlar o processo de processamento do Photoshop (semelhante às alterações para adicionar uploads de arquivo).

Implementado `setImageMaps` e `setZoomTargets` operações.

Implementado `ViewerPreset` operações. Os tipos reconhecidos são:

* `VideoPlayer` (O vídeo publica apenas esses visualizadores.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

As capas do visualizador aceitam dois parâmetros: `skinFg` e `skinBg`. O código de backend faz todo o processamento necessário para manter a compatibilidade com versões anteriores.

Implementado `getAssociatedAssets` operação.

Adicionado `ReprocessAssets` tipo de processo para permitir o reprocessamento de arquivos de origem primária carregados anteriormente, incluindo a nova cópia de PDF e a reotimização de imagens.

Renomeado `PropertySetType` tipo de campo para `propertyType`. Essa renomeação afeta o `createPropertySetType` parâmetro e `getPropertySetType/getPropertySetTypes` resposta.

Implementado `batchSetImageFields` operação para oferecer suporte à configuração de dados de usuário de imagem e outros campos de imagem editáveis.

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

Implementado `getActivePublishContexts` operação. Esta operação retorna uma matriz de nomes de contexto de publicação com servidores de publicação ativos para a empresa especificada. Os nomes do contexto de publicação atual são:

* `ImageServing`
* `ImageRendering`
* `Video`

Implementado `getSearchStrings` operação. Ele retorna uma matriz de sequências de caracteres de pesquisa para o ativo fornecido.

Adição de parâmetros de localidade para trabalhos e um mecanismo para definir a localidade para operações de API. A cadeia de caracteres local deve ser formatada como `<language_code>[-<country_code>]`. O código de idioma é um código de duas letras em minúsculas, conforme especificado pela ISO-639, e o código opcional de país é um código de duas letras em maiúsculas, conforme especificado pela ISO-3166.

Adição do parâmetro de localidade opcional ao `authHeader` Cabeçalho SOAP para definir a localidade das operações de API. Se esse parâmetro não estiver presente, o cabeçalho HTTP `Accept-Language` é usada. Se esse cabeçalho também não estiver presente, o local padrão do servidor IPS será usado.

Adição de suporte get/set para campos de metadados fortemente tipados.

Implementação de suporte a cabeçalho SOAP e HTTP para controle de resposta gzip.

Adicionado `gzipResponse` sinalizador para `authHeader`. Se não estiver presente, a API verificará o HTTP `Accept-Encoding` cabeçalho.

Adição de suporte a searchAssets para condições de campo de metadados fortemente tipados.

* Para todos os tipos de campo, o valor pode ser passado com um operador de comparação de sequência ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Para campos booleanos, `boolVal` pode ser passado com o `Equals` op
* Para campos Int, `longVal` pode ser passado com um operador de comparação numérica ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`ou `minLong/maxLong` pode ser passado com operações de intervalo numérico ( `Between, NotBetween`).
* Para campos flutuantes, `doubleVal` pode ser passado com um operador de comparação numérica ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`ou `minDouble/maxDouble` pode ser passado com operações de intervalo numérico ( `Between, NotBetween`).
* Para campos de Data, você pode passar `dateVal` com um operador de comparação numérica ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou você pode passar minDate/maxDate com operações de intervalo numérico ( `Between, NotBetween`).

Adição de descrição, `jobSubType`, e `originalJobName` campos a `JobLog` tipo.

* `originalJobName` é o nome do processo enviado a `submitJob` (sem quaisquer sufixos de exclusividade ou nomes de trabalho complementares).
* `jobSubType` é usado somente por `ImageServingPublishJob` tarefas (onde é uma de `full`, `increment, fullwithsearch,` ou `fulloverride`).
* `description` é uma cadeia de caracteres vazia para todos os tipos de trabalho, mas eventualmente contém informações resumidas do trabalho, como o caminho de upload.

Além disso, os seguintes campos não estão incluídos com ambos `getJobLogs` e `getJobLogDetails`. Em versões anteriores, eles só estavam disponíveis com `getJobLogDetails`.

* `endDate` (se o processo tiver sido concluído).
* `fileDuplicateCount` (anteriormente, era sempre `0` com `getJobLogs`)
* `fileUpdateCount` (anteriormente era sempre `0` com `getJobLogs` e incluído em `fileSuccessCount`; agora ele é dividido em campos separados).

Adição do campo assetHandle a `JobLogDetail` tipo.

Adição do parâmetro de descrição opcional a `submitJob`. Esse parâmetro é transmitido para recuperação no `getScheduledJobs`, `getActiveJobs`, e `getJobLogs`.

O campo do sistema SKU foi descontinuado. O campo é ignorado se for passado como um `SystemFieldCondition` para `searchAssets`.

Adicionado `excludeAssetTypeArray` filtrar para `searchAssets`.

Adicionado `MaskInfo` digite para `Asset`.

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

Adicionadas opções adicionais a `UploadDirectoryJob` e `UploadUrlsJob` para controlar o processamento de arquivos Postscript, Illustrator e PDF independentemente. Todas as tarefas existentes fornecem os parâmetros necessários para cada um dos três pipelines de processamento, para que funcionem exatamente como hoje. O original `PostScriptOptions` O bloco é usado para definir o processamento de arquivos Illustrator e EPS/PS. Opcionalmente, blocos de opções de arquivo específicos podem ser fornecidos para especificar o processamento. A lista de alterações inclui:

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
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rasterizar </span>(padrão) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Gerencie somente o ativo e não crie derivados após o upload. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Renderize o arquivo EPS e PostScript em uma imagem com a resolução e o espaço de cor prescritos. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Opcional. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
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
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
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
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterizando a resolução. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espaço de cor de destino para renderização. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define se um PDF de várias páginas deve ser combinado em um eCatalog após a renderização (o padrão é verdadeiro). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define se as palavras do PDF são extraídas no banco de dados para fornecimento posterior a um servidor de pesquisa (o padrão é falso). </p> </td> 
  </tr> 
 </tbody> 
</table>

Você também pode consultar de `getScheduledJobs`.

Modificou o `webservice.gzip.response` propriedade de configuração para assumir um dos seguintes valores:

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
