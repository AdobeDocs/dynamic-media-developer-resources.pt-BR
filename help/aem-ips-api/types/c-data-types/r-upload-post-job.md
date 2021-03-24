---
description: Usa getActiveJobs para rastrear uploads de desktop.
solution: Experience Manager
title: UploadPostJob
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---


# UploadPostJob{#uploadpostjob}

Usa getActiveJobs para rastrear uploads de desktop.

Consulte também [Fazer upload de ativos por meio de POSTs HTTP para o upload...](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>Todas as solicitações de POST para um trabalho de upload devem se originar do mesmo endereço IP.

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
   <td colname="col4"> <p>Opções para recortes automáticos de imagens com base em cores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Matriz de scripts de geração de conjunto automático a serem aplicados em arquivos carregados. </p> </td> 
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
   <td colname="col4"> <p>Opções que podem ser especificadas durante um upload. O conjunto afeta como a cor é gerenciada para o upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Sim</b> </p> </td> 
   <td colname="col4"> <p>Criar uma máscara. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><b>Sim</b> </p> </td> 
   <td colname="col4"> <p>Escolha das configurações de email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:InDesignOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções para carregar arquivos do InDesign no Servidor de imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções para fazer upload de arquivos Illustrator no Servidor de imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Mascarar o plano de fundo de imagens selecionadas. Isso permite que você as sobreponha em outras camadas com uma transparência fora da imagem do assunto. Opcional. </p> <p>Consulte<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções para culturas manuais de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:MediaOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções que permitem definir uma imagem em miniatura no vídeo. </p> <p>Consulte <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> substituir</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Sim</p> </td> 
   <td colname="col4"> <p>Se os arquivos devem ser sobrescritos durante o upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PDFOoptions</span> </td> 
   <td colname="col3"> <p>Não</p> </td> 
   <td colname="col4"> <p>Opções para fazer upload de arquivos PDF no Servidor de imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:Opções do Photoshop</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções para fazer upload de arquivos Photoshop no Servidor de imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>O URL onde os arquivos estão sendo carregados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções para fazer upload de arquivos Post Script para o Servidor de imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Controla a preservação de qualquer definição de cultura existente. O padrão é verdadeiro.</p> <p>Se você fornecer o parâmetro manualCropOptions e os valores correspondentes, os novos valores (excluindo 0,0,0,0) serão aplicados ao ativo independentemente do valor preserveCrop.</p><p>Se você <i>not</i> fornecer o parâmetro manualCropOptions , o valor de preserveCrop será mantido. E, em caso de true, os valores preserveCrop existentes são mantidos; no caso de false, os valores preserveCrop serão removidos.</p><p>Exemplo:</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />    &lt;left&gt;190&lt;/left&gt;<br />    &lt;right&gt;310&lt;/right&gt;<br />    &lt;top&gt;160&lt;/top&gt;<br />    &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Sim</b> </p> </td> 
   <td colname="col4"> <p>Controla se o estado de publicação de um ativo existente é preservado durante a substituição. Se não estiver definido, a configuração padrão da empresa será usada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:HandleArray</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Matriz de identificadores de projetos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Sim</b> </p> </td> 
   <td colname="col4"> <p>Se os arquivos estão marcados como prontos para publicação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:UnnCompressOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Extraia e processe o conteúdo dos arquivos TAR/ZIP carregados com essas configurações opcionais. </p> <p>Consulte <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> DescompactarOpções</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:UnsharkMaskOptions</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Opções que permitem controlar as configurações de máscara de nitidez ao criar um arquivo TIF de pirâmide otimizado. Use essas configurações para ajudar a melhorar a nitidez da imagem. </p> <p>Consulte <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharkMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Uma opção de metadados adicional para tudo no trabalho de upload. </p> </td> 
  </tr> 
 </tbody> 
</table>

