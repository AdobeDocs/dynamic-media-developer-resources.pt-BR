---
description: Faz upload de arquivos de diretórios de servidor especificados de forma recorrente.
solution: Experience Manager
title: UploadDirectoryJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a23f1bc2-aa6a-4c1d-aab5-7f6dbd08682c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# [!DNL UploadDirectoryJob]{#uploaddirectoryjob}

Faz upload de arquivos de diretórios de servidor especificados de forma recorrente.

Sintaxe

## Parâmetros {#section-69c07f4e7b2e4a0fba143ffaa9f4d48f}

<table id="table_6E40A78846F444BDB8E437413B90CFCE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoColorOptions</span> </td> 
   <td colname="col3"> <p>Opções de corte automático da imagem (com base na cor). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>Matriz de scripts de geração de conjunto automático a ser aplicada aos arquivos carregados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>Remove o espaço em branco das bordas das imagens, com base na transparência. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>Opções que você pode especificar durante um upload. O conjunto afeta como a cor é gerenciada para o upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Se uma máscara deve ser criada durante o upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Pasta IPS dos arquivos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Opção de configurações de email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> opçõesDoIlustrador</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>Opções para fazer upload de arquivos Illustrator no servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Se as subpastas devem ser incluídas durante o upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:InDesignOptions</span> </td> 
   <td colname="col3"> <p>Opções para carregar arquivos InDesign no servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>Mascarar o plano de fundo das imagens selecionadas. Isso permite que você as sobreponha em outras camadas com uma transparência fora da imagem do assunto. </p> <p>Opcional. </p> <p>Consulte <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>Opções de corte manual da imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:MediaOptions</span> </td> 
   <td colname="col3"> <p>Opções que permitem definir uma imagem em miniatura do vídeo. </p> <p>Consulte <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> substituir</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Opções de substituição de upload de arquivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PDFOptions</span> </td> 
   <td colname="col3"> <p>Opções para fazer upload de arquivos PDF no servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>Opções para fazer upload de arquivos Photoshop no servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>O URL do destino de upload de arquivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublish</span> </span>Trabalho </td> 
   <td colname="col2"> <span class="codeph"> tipos:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> <p>Detalhes de um trabalho de publicação de renderização de imagem que é executado após a conclusão do upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ImageServingPublishJob</span> </td> 
   <td colname="col3"> <p>Detalhes de um trabalho de publicação do servidor de imagens executado depois que o upload é concluído. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Se carregar somente arquivos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>Opções para fazer upload de arquivos de Post Script no servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:VideoPublishJob</span> </td> 
   <td colname="col3"> <p>Detalhes de um trabalho de publicação de vídeo executado após a conclusão do upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Controla a preservação de qualquer definição de cultura existente. O padrão é true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Controla se o estado de publicação de um ativo existente é preservado ao substituir. Se não estiver definido, a configuração padrão da empresa será usada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> processMetadataFiles</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Se arquivos XML de metadados separados devem ser processados para esse processo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:HandleArray</span> </td> 
   <td colname="col3"> <p>Matriz de identificadores de projeto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Determina se os arquivos estão marcados como prontos para publicação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDir</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>diretório de upload do Source. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:UnCompressOptions</span> </td> 
   <td colname="col3"> <p>Extraia e processe o conteúdo de arquivos TAR/ZIP carregados com essas configurações opcionais. </p> <p>Consulte <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>Opções que permitem controlar as configurações da Tirar nitidez da máscara ao criar um arquivo TIF de pirâmide otimizado. Use essas configurações para ajudar a melhorar a nitidez da imagem. </p> <p>Consulte <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html?lang=pt-BR"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Uma opção de metadados adicionais para tudo no trabalho de upload </p> </td> 
  </tr> 
 </tbody> 
</table>

## Notas {#section-637405ff7e0b4a71b83fd359b92fa0c2}

Para `CropOptions`, você pode escolher apenas um dos seguintes:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Para `PublishJob`, você pode escolher apenas um dos seguintes:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`
