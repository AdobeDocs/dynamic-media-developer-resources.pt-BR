---
description: Os materiais de cobertura de janelas incluem ambas as coberturas de janelas suaves (cortinas, valances, cortinas de café), bem como revestimentos duros de janelas (sombras e persianas).
seo-description: Os materiais de cobertura de janelas incluem ambas as coberturas de janelas suaves (cortinas, valances, cortinas de café), bem como revestimentos duros de janelas (sombras e persianas).
seo-title: Coberturas de janelas
solution: Experience Manager
title: Coberturas de janelas
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3d74466a-b7c3-43b0-9b0b-f8bb809e2773
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# Coberturas de janelas{#window-coverings}

Os materiais de cobertura de janelas incluem ambas as coberturas de janelas suaves (cortinas, valances, cortinas de café), bem como revestimentos duros de janelas (sombras e persianas).

Os materiais de revestimento de janelas especificam um arquivo de estilo *janela que abrange* ( [!DNL .vnw] extensão de ficheiro), um ficheiro de dados especial semelhante a uma vinheta, que contém dados de máscara, iluminação, disposição e textura que definem a cobertura da janela.

[!DNL vnw] os arquivos não incluem a cor e a textura (malha) para a cobertura da janela. Essas informações são especificadas separadamente, de modo semelhante às texturas repetíveis.

Os materiais que abrangem janelas só podem ser aplicados a Objetos de quadro de cobertura de janela, que são objetos sobrepostos.

<table id="table_545865B054E84592BDAEDA57DBFAE9B3"> 
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
   <td colname="col2"> <p>Janela que abrange o ficheiro de estilo; obrigatório. </p> </td> 
   <td colname="col3"> <p>Nenhum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Arquivo de imagem de textura (segundo valor para <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Nenhum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Resolução de textura. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> atributo::Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> again=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Modo de repetição. </p> </td> 
   <td colname="col3"> <p>0 (repetição direta) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Cor sólida (ou colorir textura). </p> </td> 
   <td colname="col3"> <p>128 (cinza neutro) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> afiado=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Nitidez. </p> </td> 
   <td colname="col3"> <p>0 (sem nitidez) </p> </td> 
  </tr> 
 </tbody> 
</table>

