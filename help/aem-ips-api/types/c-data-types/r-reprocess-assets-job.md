---
description: Tipo de trabalho para permitir o reprocessamento de arquivos mestres carregados anteriormente, incluindo a repetição de PDFs e a reotimização de imagens.
seo-description: Tipo de trabalho para permitir o reprocessamento de arquivos mestres carregados anteriormente, incluindo a repetição de PDFs e a reotimização de imagens.
seo-title: ReprocessAssetsJob
solution: Experience Manager
title: ReprocessAssetsJob
topic: Scene7 Image Production System API
uuid: 5b4aa838-0fb4-4ae8-be5a-8ce1e1487127
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ReprocessAssetsJob{#reprocessassetsjob}

Tipo de trabalho para permitir o reprocessamento de arquivos mestres carregados anteriormente, incluindo a repetição de PDFs e a reotimização de imagens.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Identificador de ativos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:booleano</span> </p> </td> 
   <td colname="col3"> <p>Se os arquivos estão marcados como prontos para publicação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:booleano</span> </p> </td> 
   <td colname="col3"> <p>Controla se o estado de publicação de um ativo existente é preservado ao substituir. Se não estiver definido, a configuração padrão da empresa será usada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:booleano</span> </p> </td> 
   <td colname="col3"> <p>Se uma máscara deve ser criada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:booleano</span> </p> </td> 
   <td colname="col3">Controla a preservação de qualquer definição de cultura existente. O padrão é <span class="codeph"> verdadeiro</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Opções de corte manual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Opções para cortes automáticos de imagens com base em cores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Remove o espaço em branco das bordas das imagens, com base na transparência. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>Opções para carregar arquivos do Photoshop no Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:Opções de PostScript</span> </p> </td> 
   <td colname="col3"> <p>Opções para carregar arquivos PostScript no Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:PDFOoptions</span> </p> </td> 
   <td colname="col3"> <p>Opções para carregar arquivos PDF no Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>Opções de arquivo de mídia A/V. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>Opções para carregar arquivos do Illustrator no Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>Opções que você pode especificar durante um upload. O conjunto afeta como a cor é gerenciada para o upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>Matriz de scripts de geração de conjunto automático a serem aplicados a arquivos carregados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Uma matriz de identificadores de projetos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Opções para configurações de email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:booleano</span> </p> </td> 
   <td colname="col3"> <p>Se deseja carregar somente arquivos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>URL para o local de carregamento do arquivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Detalhes da tarefa para uma tarefa de publicação de serviço de imagem a ser executada após a conclusão do upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Detalhes do trabalho para um trabalho de publicação de renderização de imagem a ser executado após a conclusão do upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Detalhes do trabalho para um trabalho de publicação de vídeo a ser executado após a conclusão do upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Opções para carregar arquivos do InDesign no servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> nocauteFundo</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Mascarar o plano de fundo das imagens selecionadas. Isso permite que você as sobreponha em outras camadas com uma transparência fora da imagem do assunto. </p> <p>Opcional. </p> <p>Consulte<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> OpçõesDePlanoDeFundoDeNivelamento</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unsharMaskOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:UnsharkMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>Opções que permitem controlar as configurações de máscara de nitidez ao criar um arquivo TIF de pirâmide otimizado. Use essas configurações para ajudar a melhorar a nitidez da imagem. </p> <p>Consulte <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_unsharp_mask_options.html"> UnnitidezMaskOptions</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Notas**

As opções para `*CropOptions` incluir:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

As opções para `*PublishJob` incluir:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

