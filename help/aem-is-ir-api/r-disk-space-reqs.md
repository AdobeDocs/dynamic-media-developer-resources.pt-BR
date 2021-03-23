---
description: 'Além do espaço necessário para instalar o software, o Image Serving tem os seguintes requisitos de espaço em disco '
solution: Experience Manager
title: Requisitos e recomendações de espaço em disco
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---


# Requisitos de espaço em disco e recomendações{#disk-space-requirements-and-recommendations}

Além do espaço necessário para instalar o software, o Image Serving tem os seguintes requisitos de espaço em disco:

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Descrição/ Local Padrão/ Definir Com</b> </th> 
   <th class="entry"> <b>Cálculo/ Recomendação</b> </th> 
   <th class="entry"> <b>Comentários</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Imagens de origem, fontes, perfis ICC</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/images  </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths  </span> </p> </td> 
   <td> <p>Varia; consulte os comentários abaixo. </p> </td> 
   <td> <p>Só precisa ser acessível ao Servidor de imagens; os servidores nunca modificam os dados. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache de dados de resposta HTTP</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/is-response  </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders  </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize  </span> x 2; pelo menos 2 GB recomendado. </p> </td> 
   <td> <p>Esse cache também armazena dados aninhados/incorporados e imagens de origem estrangeira. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache de dados do catálogo de imagens</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/catalog  </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder  </span> </p> </td> 
   <td> <p>Permitir que a pasta de catálogo use 1,5 vezes o espaço. </p> </td> 
   <td> <p>Preenchido quando os catálogos são carregados inicialmente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Dados de log</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/logs  </span> </p> <p> <span class="codeph"> PS::LogFolder  </span> </p> <p> <span class="codeph"> IS::LogFile  </span> </p> <p> <span class="codeph"> SV::LogFile  </span> </p> </td> 
   <td> <p>100 Mbytes ou mais. </p> </td> 
   <td> <p>Varia dependendo da configuração de registro e do uso do servidor. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Arquivos temporários do servidor de imagens</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/temp  </span> </p> <p> <span class="codeph"> IS::TempDirectory  </span> </p> <p> <span class="codeph"> SV::TempDirectory  </span> </p> </td> 
   <td> <p>100 MBytes é suficiente para a maioria dos usos. </p> </td> 
   <td> <p>Dados de curta duração; pode ser necessário para imagens de origem diferentes de PTIFF e determinados formatos de imagem de resposta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisitos de espaço em disco para imagens de origem {#section-317da75099ad480d9a461c7e706d4f1c}

É recomendável converter todas as imagens de origem para o formato de arquivo TIFF (PTIFF) da pirâmide usando a ferramenta de linha de comando (IC) do Conversor de imagem. Essa conversão garante o desempenho ideal em tempo de execução do Serviço de imagem para todos os aplicativos. Embora o Servidor de Imagem possa processar todos os formatos de arquivo de origem aceitos pelo IC, o Dynamic Media não fornece suporte para esses usos.

Quando você usa arquivos PTIFF, as seguintes regras básicas podem ajudá-lo a determinar os requisitos de espaço.

*`total_space`* (bytes) =  *`number_of_images`* x(2000 +  *`avg_pixel_count`* x  *`avg_num_components`* x  *`p_factor`*)

* *`avg_pixel_count`* O tamanho médio de pixel (largura x altura) de todas as imagens de origem originais. Por exemplo, se as imagens originais tipicamente estivessem em torno de 2k x 2k pixels, isso seria 4M pixels.
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
   <td> <p> 33º </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Deflate-Compression </p> </td> 
   <td> <p> 25-0,75, dependendo da imagem </p> </td> 
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

Uma implantação do Image Serving espera usar 30.000 imagens herdadas de baixa resolução, com um tamanho médio de 500x500 pixels RGB. Espera-se que novos dados de imagem de qualidade de impressão sejam adicionados a uma taxa de 10.000 por ano. O tamanho típico da imagem CMYK será de 4k x 6k bytes. Todos os dados serão compactados em JPEG de alta qualidade. A quantidade total de espaço em disco após 3 anos de utilização é estimada da seguinte forma:

*`total_space`* = 30.000 x (2k + 0,5k x 0,5k x 3 x 0,1) + 3 x 10.000 x (2k + 4k x 6k x 4 x 0,1) = 2,2 G + 268 GB = aproximadamente 270 GB

Para uma melhor qualidade garantida, poderia ser utilizada a compressão deflate (zip). Considerando um *`p_factor`* de 0,4, a quantidade total de espaço em disco necessária é aproximadamente 4 vezes maior. Nesse caso, pouco mais de 1 TB.
