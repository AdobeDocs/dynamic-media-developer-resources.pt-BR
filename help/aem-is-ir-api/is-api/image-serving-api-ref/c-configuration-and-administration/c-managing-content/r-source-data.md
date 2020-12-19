---
description: Os arquivos de dados de origem do Servidor de imagens incluem arquivos de imagem e máscara, fontes e perfis ICC.
seo-description: Os arquivos de dados de origem do Servidor de imagens incluem arquivos de imagem e máscara, fontes e perfis ICC.
seo-title: Dados de origem
solution: Experience Manager
title: Dados de origem
topic: Scene7 Image Serving - Image Rendering API
uuid: d654eee7-ef2d-4546-93bb-72f80c38e018
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# Dados de origem{#source-data}

Os arquivos de dados de origem do Servidor de imagens incluem arquivos de imagem e máscara, fontes e perfis ICC.

Todos os arquivos de dados de origem devem estar acessíveis ao Servidor de imagens. O Serviço de imagem fornece várias alternativas para especificar a localização dos arquivos de dados:

` *`install_`*/ *``*/ *`folderrootPathFilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath  </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> CatalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> CatalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catálogo::Caminho|catálogo::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> caminho e nome do arquivo de imagem relativo especificados em uma solicitação HTTP de disponibilização de imagem</span> </p></td> 
 </tr> 
</table>

O servidor combina segmentos de caminho da direita para a esquerda até que um caminho de arquivo absoluto seja estabelecido.

Todos os segmentos ` *`rootPath`*` podem ser segmentos de caminho vazios, relativos ou absolutos.

` *``*` CatalogPathis é um caminho/nome de arquivo absoluto ou relativo. ` *``*` requestPath deve ser um caminho/nome de arquivo relativo.

`Multiple IS::RootPath` os valores podem ser definidos em ImageServerRegistry.xml (ou por meio da interface do administrador). Isso permite que os arquivos de dados de origem sejam distribuídos em vários sistemas de arquivos. O Servidor de imagens tentará caminhos alternativos na ordem especificada até que o arquivo de dados seja encontrado.

Novos arquivos de dados de qualquer tipo podem ser adicionados a qualquer momento sem interromper o servidor.
