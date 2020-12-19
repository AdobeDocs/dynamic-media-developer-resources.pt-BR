---
description: Um material é considerado uma borda de parede quando especificado em uma borda de parede MSS (introduzido com sub=3.5).
seo-description: Um material é considerado uma borda de parede quando especificado em uma borda de parede MSS (introduzido com sub=3.5).
seo-title: Bordas de mural
solution: Experience Manager
title: Bordas de mural
topic: Scene7 Image Serving - Image Rendering API
uuid: 40acd667-5e8b-4425-b44a-0681e608d189
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# Bordas do mural{#wall-borders}

Um material é considerado uma borda de parede quando especificado em uma borda de parede MSS (introduzido com sub=3.5).

As imagens de textura da borda do mural podem incluir um canal alfa para definir a forma da borda. Bordas de mural só podem ser aplicadas a objetos de mural.

<table id="table_906C5CC4CADF4024AA0E29544AF48080"> 
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
   <td colname="col2"> <p>Imagem de textura repetível; required </p> </td> 
   <td colname="col3"> <p>Nenhum </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Resolução de textura </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> atributo::Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> âncora=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Alinhamento da textura horizontal (o valor y é ignorado) </p> </td> 
   <td colname="col3"> <p>0 (borda da imagem esquerda) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> afiado=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Nitidez </p> </td> 
   <td colname="col3"> <p>0 (sem nitidez) </p> </td> 
  </tr> 
 </tbody> 
</table>

