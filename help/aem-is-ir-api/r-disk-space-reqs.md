---
description: 'Além do espaço necessário para instalar o software, o serviço de imagem tem os seguintes requisitos de espaço em disco '
seo-description: 'Além do espaço necessário para instalar o software, o serviço de imagem tem os seguintes requisitos de espaço em disco '
seo-title: Requisitos e recomendações de espaço em disco
solution: Experience Manager
title: Requisitos e recomendações de espaço em disco
topic: Scene7 Image Serving - Image Rendering API
uuid: a6a21886-94d6-45b3-af68-497e039bdbac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---


# Requisitos e recomendações de espaço em disco{#disk-space-requirements-and-recommendations}

Além do espaço necessário para instalar o software, o Serviço de imagem tem os seguintes requisitos de espaço em disco:

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Descrição/ Localização Padrão/ Definir com</b> </th> 
   <th class="entry"> <b>Cálculo/ Recomendação</b> </th> 
   <th class="entry"> <b>Comentários</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Imagens de origem, fontes, perfis ICC</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/images  </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths  </span> </p> </td> 
   <td> <p>Varia; veja os comentários abaixo. </p> </td> 
   <td> <p>Só precisa ser acessível ao servidor de imagens; os servidores nunca modificam os dados. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache de dados de resposta HTTP</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/is-response  </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders  </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize  </span> x 2; recomenda-se pelo menos 2 GB. </p> </td> 
   <td> <p>Esse cache também armazena dados aninhados/incorporados e imagens de origem estrangeira. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache de dados do catálogo de imagens</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/Catalog  </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder  </span> </p> </td> 
   <td> <p>Permita que a pasta de catálogo use 1,5x o espaço. </p> </td> 
   <td> <p>Preenchido quando os catálogos são carregados inicialmente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Dados de registro</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/logs  </span> </p> <p> <span class="codeph"> PS::LogFolder  </span> </p> <p> <span class="codeph"> IS::LogFile  </span> </p> <p> <span class="codeph"> SV::LogFile  </span> </p> </td> 
   <td> <p>100 Mbytes ou mais. </p> </td> 
   <td> <p>Varia dependendo da configuração de registro e do uso do servidor. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Arquivos temporários do Servidor de imagens</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/temp  </span> </p> <p> <span class="codeph"> IS::TempDirectory  </span> </p> <p> <span class="codeph"> SV::TempDirectory  </span> </p> </td> 
   <td> <p>100 MBytes é suficiente para a maioria dos usos. </p> </td> 
   <td> <p>Dados de vida curta; pode ser necessário para imagens de origem que não sejam PTIFFs e determinados formatos de imagem de resposta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisitos de espaço em disco para imagens de origem {#section-317da75099ad480d9a461c7e706d4f1c}

É recomendável converter todas as imagens de origem no formato de arquivo TIFF (PTIFF) da pirâmide usando a ferramenta de linha de comando (IC) do Conversor de imagens. Essa conversão garante o desempenho ideal de tempo de execução do Serviço de imagem para todos os aplicativos. Embora o Servidor de imagens possa processar todos os formatos de arquivo de origem aceitos pelo IC, a Scene7 não fornece suporte para esses usos.

Quando você usa arquivos PTIFF, as seguintes regras de miniatura podem ajudá-lo a determinar os requisitos de espaço.

*`total_space`* (bytes) =  *`number_of_images`* x(2000 +  *`avg_pixel_count`* x  *`avg_num_components`* x  *`p_factor`*)

* *`avg_pixel_count`* O tamanho médio de pixel (largura x altura) de todas as imagens de origem originais. Por exemplo, se as imagens originais tipicamente estiverem em torno de 2k x 2k pixels, isso seria de 4M pixels.
* *`avg_num_components`* Depende do tipo de imagens. Na maioria das imagens RGB, é 3, na maioria das imagens CMYK ou RGBA, é 4. Use 3,5 se metade das imagens for RGB e a outra metade for RGBA.
* *`p_factor`* Depende do tipo de compactação e do conjunto de qualidade quando as imagens são convertidas com IC.

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Compactação PTIFF</b> </th> 
   <th class="entry"> <b><i>p_fator</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Descompactado </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Deflate-Compression </p> </td> 
   <td> <p> 25-0.75, dependendo da imagem </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Compactação JPEG </p> </td> 
   <td> <p> 1 (típico para JPEG de qualidade 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Essa aproximação não contabiliza a sobrecarga do sistema de arquivos. O espaço real no disco pode ser substancialmente maior.

**Exemplo**

Uma implantação do Serviço de imagens espera usar 30.000 imagens herdadas de baixa resolução, com um tamanho médio de 500 x 500 pixels RGB. Espera-se que novos dados de imagem de qualidade de impressão sejam adicionados a uma taxa de 10.000 por ano. O tamanho de imagem CMYK típico será de 4k x 6k bytes. Todos os dados serão compactados em JPEG de alta qualidade. A quantidade total de espaço em disco após 3 anos de utilização é estimada do seguinte modo:

*`total_space`* = 30.000 x (2 k + 0,5 k x 0,5 k x 3 x 0,1) + 3 x 10.000 x (2 k + 4 k x 6 k x 4 x 0,1) = 2,2 G + 268 GB = aproximadamente 270 GB

Para a melhor qualidade garantida, poderia ser usada a compactação deflate (zip). Presumindo um *`p_factor`* de 0,4, a quantidade total de espaço em disco necessária é aproximadamente 4 vezes maior. Nesse caso, pouco mais de 1 TB.
