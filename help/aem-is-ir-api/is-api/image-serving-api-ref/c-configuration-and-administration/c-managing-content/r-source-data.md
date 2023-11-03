---
description: Os arquivos de dados de origem do Servidor de imagens incluem arquivos de imagem e máscara, fontes e perfis ICC.
solution: Experience Manager
title: Dados de origem
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Dados de origem{#source-data}

Os arquivos de dados de origem do Servidor de imagens incluem arquivos de imagem e máscara, fontes e perfis ICC.

Todos os arquivos de dados de origem devem estar acessíveis ao Servidor de imagens. O Servidor de imagens fornece várias alternativas para especificar o local dos arquivos de dados:

`*`install_folder`*/ *`rootPath`*/ *`filePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> caminho relativo do arquivo de imagem e nome especificados em uma solicitação HTTP do Servidor de imagens</span> </p></td> 
 </tr> 
</table>

O servidor combina segmentos de caminho da direita para a esquerda até que um caminho de arquivo absoluto seja estabelecido.

Todos `*`rootPath`*` os segmentos podem ser segmentos de caminho vazios, relativos ou absolutos.

`*`catalogPath`*` é um caminho/nome de arquivo absoluto ou relativo. `*`requestPath`*` deve ser um caminho/nome de arquivo relativo.

`Multiple IS::RootPath` Os valores de podem ser definidos em ImageServerRegistry.xml (ou por meio da interface de administrador). Isso permite que os arquivos de dados de origem sejam distribuídos em vários sistemas de arquivos. O Servidor de imagens tenta caminhos alternativos na ordem especificada, até que o arquivo de dados seja encontrado.

Novos arquivos de dados de qualquer tipo podem ser adicionados a qualquer momento sem interromper o servidor.
