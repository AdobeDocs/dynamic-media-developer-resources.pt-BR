---
description: As texturas repetidas incluem materiais interiores e exteriores, como tecidos (vestuário e estofos), revestimentos de pavimentos de parede para parede, papéis de parede, materiais de contraplacado, texturas de grãos de madeira, revestimentos e materiais laterais, e qualquer outra textura genérica.
seo-description: As texturas repetidas incluem materiais interiores e exteriores, como tecidos (vestuário e estofos), revestimentos de pavimentos de parede para parede, papéis de parede, materiais de contraplacado, texturas de grãos de madeira, revestimentos e materiais laterais, e qualquer outra textura genérica.
seo-title: Texturas repetidas
solution: Experience Manager
title: Texturas repetidas
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 11a55d9f-a1d7-490e-af0e-9bf2c3a35501
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---


# Texturas repetidas{#repeatable-textures}

As texturas repetidas incluem materiais interiores e exteriores, como tecidos (vestuário e estofos), revestimentos de pavimentos de parede para parede, papéis de parede, materiais de contraplacado, texturas de grãos de madeira, revestimentos e materiais laterais, e qualquer outra textura genérica.

Texturas repetidas podem ser aplicadas a objetos planos, de linha flutuante, de rascunho, de plano, de parede e de gabinete. Quando aplicado a um objeto sem textura, o objeto é pintado com `color=` (ou `bgc=` se `color=` não for especificado).

Um material é considerado uma textura se incluir um atributo `src=` especificando uma imagem e se ocorrer em um MSS diferente de uma borda de decal ou de parede.

Ao renderizar, a textura é alinhada com o objeto ao corresponder o ponto `anchor=` do material de textura ao ponto de origem de textura do objeto (como criado na vinheta).

<table id="table_992A6E93E4274B598A236F8F728F017A"> 
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
   <td colname="col3"> <p>Nenhum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Resolução de textura </p> </td> 
   <td colname="col3"> <span class="codeph"> atributo::Resolution  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> âncora=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Ponto de alinhamento da textura </p> </td> 
   <td colname="col3"> <p>Canto superior esquerdo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> again=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Modo Repetir </p> </td> 
   <td colname="col3"> <p>0 (repetição direta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> afiado=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Nitidez </p> </td> 
   <td colname="col3"> <p>0 (sem nitidez). </p> </td> 
  </tr> 
 </tbody> 
</table>

Além desses atributos básicos, texturas repetíveis suportam os seguintes atributos de propósito especial para aplicativos avançados:

<table id="table_A97365804CB143DEB31F26A65DA3CE04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Atributo </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
   <th colname="col3" class="entry"> <p>Padrão </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> grout=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Cor e espessura do grupo; útil para materiais cerâmicos/azulejos de pedra </p> </td> 
   <td colname="col3"> <p>Grupo já presente na imagem </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Modo de alinhamento (entre objetos); usado para aplicativos de estofo </p> </td> 
   <td colname="col3"> <p>Correspondência central </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Ângulo de rotação da textura; não suportado por objetos de parede </p> </td> 
   <td colname="col3"> <p>0 (sem rotação) </p> </td> 
  </tr> 
 </tbody> 
</table>

