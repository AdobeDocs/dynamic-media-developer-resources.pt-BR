---
description: Usa getActiveJobs para rastrear os uploads da área de trabalho.
seo-description: Usa getActiveJobs para rastrear os uploads da área de trabalho.
seo-title: UploadPostJob
solution: Experience Manager
title: UploadPostJob
topic: Scene7 Image Production System API
uuid: 172f47c7-685a-4014-9c30-dacd78733655
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UploadPostJob{#uploadpostjob}

Usa getActiveJobs para rastrear os uploads da área de trabalho.

Consulte também [Fazer upload de ativos por meio de HTTP POSTs para fazer upload...](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>Todas as solicitações POST para um trabalho de upload devem se originar do mesmo endereço IP.

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col03" class="entry"> <p>Obrigatório? </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoColorCropOptions</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Opções para cortes automáticos de imagens com base em cores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoSetCreateOptions</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Matriz de scripts de geração de conjunto automático a serem aplicados a arquivos carregados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoTransparentCropOptions</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Remove o espaço em branco das bordas das imagens, com base na transparência. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ColorManagementOptions</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Opções que você pode especificar durante um upload. O conjunto afeta como a cor é gerenciada para o upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col03"> <p><b>Sim</b> </p> </td> 
   <td colname="col3"> <p>Se uma máscara deve ser criada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col03"> <p><b>Sim</b> </p> </td> 
   <td colname="col3"> <p>Escolha das configurações de email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:InDesignOptions</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Opções para carregar arquivos do InDesign no Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:IllustratorOptions</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Opções para carregar arquivos do Illustrator no Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nocauteFundo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:KnockoutBackgroundOptions</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Mascarar o plano de fundo das imagens selecionadas. Isso permite que você as sobreponha em outras camadas com uma transparência fora da imagem do assunto. Opcional. </p> <p>Consulte<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ManualCropOptions</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Opções para cortes manuais de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:MediaOptions</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Opções que permitem definir uma imagem em miniatura a partir do vídeo. </p> <p>Consulte <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> substituir</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col03"> <p><b>Sim</b> </p> </td> 
   <td colname="col3"> <p>Se os arquivos devem ser sobrescritos durante o upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PDFOoptions</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Opções para carregar arquivos PDF no Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PhotoshopOptions</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Opções para carregar arquivos do Photoshop no Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>O URL no qual os arquivos estão sendo carregados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:Opções de PostScript</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Opções para carregar arquivos Post Script no Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Controla a preservação de qualquer definição de cultura existente. Os padrões são verdadeiros. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col03"> <p><b>Sim</b> </p> </td> 
   <td colname="col3"> <p>Controla se o estado de publicação de um ativo existente é preservado ao substituir. Se não estiver definido, a configuração padrão da empresa será usada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:HandleArray</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Matriz de identificadores de projetos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col03"> <p><b>Sim</b> </p> </td> 
   <td colname="col3"> <p>Se os arquivos estão marcados como prontos para publicação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:UnCompressOptions</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Extraia e processe o conteúdo dos arquivos TAR/ZIP carregados com essas configurações opcionais. </p> <p>Consulte <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> DescompactarOpções</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharMaskOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:UnsharkMaskOptions</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Opções que permitem controlar as configurações de máscara de nitidez ao criar um arquivo TIF de pirâmide otimizado. Use essas configurações para ajudar a melhorar a nitidez da imagem. </p> <p>Consulte <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnnitidezMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col03"> <p>Não </p> </td> 
   <td colname="col3"> <p>Uma opção de metadados adicional para tudo no trabalho de upload. </p> </td> 
  </tr> 
 </tbody> 
</table>

