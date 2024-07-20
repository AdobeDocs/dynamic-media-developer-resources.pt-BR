---
title: Coberturas de janelas
description: Os materiais de revestimento de janelas incluem tanto revestimentos de janelas macias (cortinas, valências, cortinas de café) como de janelas duras (sombras e persianas).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce6543a1-2438-4661-95bf-ff3d956013bc
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# Coberturas de janelas{#window-coverings}

Os materiais de revestimento de janelas incluem tanto revestimentos de janelas macias (cortinas, valências, cortinas de café) como de janelas duras (sombras e persianas).

Os materiais de cobertura de janelas especificam um *arquivo de estilo de cobertura de janelas* (extensão de arquivo [!DNL .vnw]), um arquivo de dados especial semelhante a uma vinheta, contendo dados de máscara, iluminação, layout e textura que definem a cobertura de janelas.

[!DNL vnw] arquivos não incluem a cor e a textura (malha) para a cobertura da janela. Essas informações são especificadas separadamente, semelhantes às texturas repetíveis.

Os materiais de revestimento de janelas só podem ser aplicados a Objetos de Quadro de Cobertura de Janelas, que são objetos sobrepostos.

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Arquivo de estilo de cobertura de janela; obrigatório. </p> </td> 
   <td colname="col3"> <p>Nenhum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Arquivo de imagem de textura (segundo valor para <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Nenhum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Resolução da textura. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> atributo::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repetir= </span> </a> </p> </td> 
   <td colname="col2"> <p>Modo de repetição. </p> </td> 
   <td colname="col3"> <p>0 (repetição direta) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> cor= </span> </a> </p> </td> 
   <td colname="col2"> <p>Cor sólida (ou colore a textura). </p> </td> 
   <td colname="col3"> <p>128 (cinza neutro) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Nitidez. </p> </td> 
   <td colname="col3"> <p>0 (sem nitidez) </p> </td> 
  </tr> 
 </tbody> 
</table>
