---
title: Requisitos e recomendações de espaço em disco
description: Além do espaço necessário para instalar o software, o Servidor de imagens tem os seguintes requisitos de espaço em disco.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Requisitos e recomendações de espaço em disco{#disk-space-requirements-and-recommendations}

Além do espaço necessário para instalar o software, o Servidor de imagens tem os seguintes requisitos de espaço em disco:

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Descrição/ Localização Padrão/ Definida Com</b> </th> 
   <th class="entry"> <b>Cálculo/ Recomendação</b> </th> 
   <th class="entry"> <b>Comentários</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Imagens, fontes e perfis ICC do Source</b> </p> <p> <span class="filepath"> <span class="varname"> pasta_de_instalação </span>/imagens </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths </span> </p> </td> 
   <td> <p>Varia; consulte os comentários abaixo. </p> </td> 
   <td> <p>Somente deve ser acessível ao Servidor de imagens; os servidores nunca modificam dados. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache de dados de resposta HTTP</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2; pelo menos 2 GB recomendados. </p> </td> 
   <td> <p>Esse cache também armazena dados aninhados/incorporados e imagens de origem estrangeira. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache de dados do catálogo de imagens</b> </p> <p> <span class="filepath"> <span class="varname"> pasta_de_instalação </span>/cache/catálogo </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>Permita que a pasta de catálogo use 1,5x o espaço. </p> </td> 
   <td> <p>Preenchido quando os catálogos são carregados inicialmente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Dados de log</b> </p> <p> <span class="filepath"> <span class="varname"> pasta_de_instalação </span>/logs </span> </p> <p> <span class="codeph"> PS::LogFolder </span> </p> <p> <span class="codeph"> IS::LogFile </span> </p> <p> <span class="codeph"> SV::LogFile </span> </p> </td> 
   <td> <p>100 MB ou mais. </p> </td> 
   <td> <p>Isso varia dependendo da configuração de registro e do uso do servidor. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Arquivos temporários do Servidor de Imagens</b> </p> <p> <span class="filepath"> <span class="varname"> pasta_de_instalação </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::TempDirectory </span> </p> </td> 
   <td> <p>100 MB são suficientes para a maioria dos usos. </p> </td> 
   <td> <p>Dados de vida curta; podem ser necessários para imagens de origem diferentes de PTIFFs e determinados formatos de imagem de resposta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisitos de espaço em disco para imagens de origem {#section-317da75099ad480d9a461c7e706d4f1c}

A Adobe recomenda converter todas as imagens de origem no formato de arquivo TIFF da pirâmide (PTIFF) usando a ferramenta de linha de comando Conversor de imagens (IC). Essa conversão garante o desempenho em tempo de execução ideal do Servidor de imagens para todos os aplicativos. Embora o Servidor de imagens possa processar todos os formatos de arquivo de origem aceitos pelo IC, o Dynamic Media não é compatível com esses usos.

Quando você usa arquivos PTIFF, as seguintes regras básicas podem ajudá-lo a determinar os requisitos de espaço.

*`total_space`* (bytes) = *`number_of_images`* × (2000 + *`avg_pixel_count`* x *`avg_num_components`* × *`p_factor`*)

* *`avg_pixel_count`* O tamanho médio em pixels (largura x altura) de todas as imagens de origem. Por exemplo, se as imagens originais são tipicamente em torno de 2k × 2k pixels, isso seria 4 megapixels.
* *`avg_num_components`* Depende do tipo de imagens. Para a maioria das imagens RGB, é 3; para a maioria das imagens CMYK ou RGBA, é 4. Use a versão 3.5 se metade das imagens for RGB e a outra metade for RGBA.
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
   <td> <p>Não compactado </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Deflate-Compression </p> </td> 
   <td> <p> 25-0,75, dependendo da imagem </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Compactação JPEG </p> </td> 
   <td> <p> 1 (típico para JPEG quality 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Essa aproximação não leva em conta a sobrecarga do sistema de arquivos. O espaço real no disco pode ser substancialmente maior.

**Exemplo**

Uma implantação do Servidor de imagens espera usar 30.000 imagens herdadas de baixa resolução, com um tamanho médio de 500 × 500 pixels RGB. Novos dados de imagem com qualidade de impressão são adicionados a uma taxa de 10.000 por ano. O tamanho típico da imagem CMYK é de 4k × 6k bytes. Todos os dados são compactados pela JPEG em alta qualidade. A quantidade total de espaço em disco após três anos de uso é estimada da seguinte maneira:

*`total_space`* = 30.000 × (2k + 0,5k × 0,5k × 3 × 0,1) + 3 × 10.000 × (2k + 4k × 6k × 4 × 0,1) = 2,2 G + 268 GB = aproximadamente 270 GB

Para garantir a melhor qualidade, uma compactação, como zip, pode ser empregada. Presumindo-se um *`p_factor`* de 0,4, a quantidade total de espaço em disco necessária é aproximadamente quatro vezes maior. Nesse caso, pouco mais de 1 terabyte.
