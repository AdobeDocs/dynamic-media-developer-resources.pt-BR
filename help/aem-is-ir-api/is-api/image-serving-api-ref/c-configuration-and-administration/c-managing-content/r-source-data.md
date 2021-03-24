---
description: Os arquivos de dados de origem do fornecimento de imagens incluem arquivos de imagem e máscara, fontes e perfis ICC.
solution: Experience Manager
title: Dados de origem
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# Dados de origem{#source-data}

Os arquivos de dados de origem do fornecimento de imagens incluem arquivos de imagem e máscara, fontes e perfis ICC.

Todos os arquivos de dados de origem devem estar acessíveis ao Servidor de Imagens. O Image Serving fornece várias alternativas para especificar a localização dos arquivos de dados:

`*`install_`*/ *``*/ *`folderrootPathPath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath  </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catálogo::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> caminho e nome do arquivo de imagem relativo especificados em uma solicitação HTTP de exibição de imagem</span> </p></td> 
 </tr> 
</table>

O servidor combina segmentos de caminho da direita para a esquerda até que um caminho de arquivo absoluto seja estabelecido.

Todos os segmentos `*`rootPath`*` podem ser segmentos de caminho vazios, relativos ou absolutos.

`*``*` catalogPathis é um caminho/nome de arquivo absoluto ou relativo. `*``*` requestPathdeve ser um caminho/nome de arquivo relativo.

`Multiple IS::RootPath` Os valores podem ser definidos em ImageServerRegistry.xml (ou por meio da interface de administrador). Isso permite que os arquivos de dados de origem sejam distribuídos em vários sistemas de arquivos. O Servidor de Imagens tentará caminhos alternativos na ordem especificada até que o arquivo de dados seja encontrado.

Novos arquivos de dados de qualquer tipo podem ser adicionados a qualquer momento sem interromper o servidor.
