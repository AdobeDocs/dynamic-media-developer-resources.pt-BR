---
description: Usa getActiveJobs para rastrear os uploads de desktop.
solution: Experience Manager
title: UploadPostJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 60163016-fe96-4ac2-9208-da8192042d0f
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# [!DNL UploadPostJob]{#uploadpostjob}

Usa getActiveJobs para rastrear os uploads de desktop.

Consulte também [Upload de ativos por meio de POSTs HTTP no Upload...](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>Todas as solicitações POST para um trabalho de upload devem se originar do mesmo endereço IP.

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obrigatório? </p> </th> 
   <th colname="col4" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoColorCropOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções para recortes automáticos de imagens com base na cor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Matriz de scripts de geração de conjunto automático a ser aplicada aos arquivos carregados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Remove o espaço em branco das bordas das imagens, com base na transparência. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções que você pode especificar durante um upload. O conjunto afeta como a cor é gerenciada para o upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p><b>Sim</b> </p> </td> 
   <td colname="col4"> <p>Se uma máscara deve ser criada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><b>Sim</b> </p> </td> 
   <td colname="col4"> <p>Opção de configurações de email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:InDesignOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções de upload de arquivos InDesign para o Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Opções do Illustrator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções de upload de arquivos Illustrator para o Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Mascarar o plano de fundo das imagens selecionadas. Isso permite que você as sobreponha em outras camadas com uma transparência fora da imagem do assunto. Opcional. </p> <p>Consulte<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções para recortes manuais de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:MediaOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções que permitem definir uma imagem em miniatura do vídeo. </p> <p>Consulte <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> substituir</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Sim</p> </td> 
   <td colname="col4"> <p>Substituir arquivos ao fazer upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PDFOptions</span> </td> 
   <td colname="col3"> <p>Não</p> </td> 
   <td colname="col4"> <p>Opções de upload de arquivos PDF para o Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções de upload de arquivos Photoshop para o Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>O URL no qual os arquivos estão sendo carregados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções para fazer upload de arquivos de Post Script no Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Controla a preservação de qualquer definição de cultura existente. O padrão é verdadeiro.</p> <p>Se você fornecer o parâmetro manualCropOptions e os valores correspondentes, os novos valores (excluindo 0,0,0,0) serão aplicados ao ativo independentemente do valor preserveCrop.</p><p>Se você <i>não</i> fornecer o parâmetro manualCropOptions, o valor de preserveCrop será mantido. E, no caso de true, os valores preserveCrop existentes são retidos; no caso de false, os valores preserveCrop são removidos.</p><p>Exemplo:</p><p><p>&lt;preserveCrop&gt;false&lt;/preserveCrop&gt;<br />&lt;manualCropOptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualCropOptions&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p><b>Sim</b> </p> </td> 
   <td colname="col4"> <p>Controla se o estado de publicação de um ativo existente é preservado ao substituir. Se não estiver definido, a configuração padrão da empresa será usada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:HandleArray</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Matriz de identificadores de projeto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p><b>Sim</b> </p> </td> 
   <td colname="col4"> <p>Se os arquivos estão marcados como prontos para publicação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:UnCompressOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Extraia e processe o conteúdo de arquivos TAR/ZIP carregados com essas configurações opcionais. </p> <p>Consulte <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções que permitem controlar as configurações da Tirar nitidez da máscara ao criar um arquivo TIF de pirâmide otimizado. Use essas configurações para ajudar a melhorar a nitidez da imagem. </p> <p>Consulte <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Uma opção de metadados adicionais para tudo no trabalho de upload. </p> </td> 
  </tr> 
 </tbody> 
</table>
