---
description: Os materiais dos gabinetes especificam um arquivo de estilo de gabinete (extensão de arquivo .vnc), um arquivo de dados especial contendo representações fotográficas de gabinetes, juntamente com definições de layout paramétrico e outras informações necessárias para renderizar fronts de gabinete.
seo-description: Os materiais dos gabinetes especificam um arquivo de estilo de gabinete (extensão de arquivo .vnc), um arquivo de dados especial contendo representações fotográficas de gabinetes, juntamente com definições de layout paramétrico e outras informações necessárias para renderizar fronts de gabinete.
seo-title: Gabinetes
solution: Experience Manager
title: Gabinetes
uuid: d515c613-07c5-49ef-ad6e-568a1f6c1335
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# Gabinetes{#cabinets}

Os materiais dos gabinetes especificam um arquivo de estilo de gabinete (extensão de arquivo .vnc), um arquivo de dados especial contendo representações fotográficas de gabinetes, juntamente com definições de layout paramétrico e outras informações necessárias para renderizar fronts de gabinete.

[!DNL vnc] os arquivos podem incluir textura repetível de grãos de madeira ou a textura pode ser fornecida externamente por meio de um segundo argumento para  `src=`. Certos arquivos [!DNL vnc] permitem colorir ou texturizar áreas selecionadas de frontas de gabinete (normalmente usadas para estilos de gabinete laminado).

Os materiais do gabinete só podem ser aplicados a objetos do gabinete.

<table id="table_0B16200886FE4DFEBB1E4BE8FBA67EE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Atributo </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
   <th colname="col3" class="entry"> <p>Padrão </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Arquivo de estilo do gabinete; obrigatório. </p> </td> 
   <td colname="col3"> <p>Nenhum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Arquivo de imagem de textura opcional (segundo valor para <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Nenhum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Resolução de textura opcional. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> atributo::Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Coloriza o gabinete e/ou a textura. </p> </td> 
   <td colname="col3"> <p>Nenhum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> shar=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Nitidez. </p> </td> 
   <td colname="col3"> <p>0 (sem nitidez) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> sinalizadores=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Sinalizadores de renderização especiais. </p> </td> 
   <td colname="col3"> <p>0 (sem sinalizadores) </p> </td> 
  </tr> 
 </tbody> 
</table>

