---
title: Texturas repetíveis
description: As texturas repetíveis incluem materiais interiores e exteriores, como tecidos (tanto vestuário como estofos), revestimentos de parede a parede para o chão, papéis de parede, materiais de bancada, texturas de grãos de madeira, materiais de telhados e laterais e qualquer outra textura genérica.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3693498b-994a-460a-8b2e-780a1482d37a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Texturas repetíveis{#repeatable-textures}

As texturas repetíveis incluem materiais interiores e exteriores, como tecidos (tanto vestuário como estofos), revestimentos de parede a parede para o chão, papéis de parede, materiais de bancada, texturas de grãos de madeira, materiais de telhados e laterais e qualquer outra textura genérica.

Texturas repetidas podem ser aplicadas a objetos planos, fluidos, rascunhos, planos, paredes e armários. Quando aplicado a um objeto não texturável, o objeto é pintado com `color=` (ou `bgc=` se `color=` não for especificado).

Um material é considerado uma textura se incluir um atributo `src=` especificando uma imagem e se ocorrer em um MSS diferente de decalque ou borda de parede.

Durante a renderização, a textura é alinhada com o objeto, combinando o ponto `anchor=` do material de textura com o ponto de origem da textura do objeto (conforme criado na vinheta).

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Imagem de textura repetível; obrigatório </p> </td> 
   <td colname="col3"> <p>Nenhum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Resolução da textura </p> </td> 
   <td colname="col3"> <span class="codeph"> atributo::Resolution </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> âncora= </span> </a> </p> </td> 
   <td colname="col2"> <p>Ponto de alinhamento de textura </p> </td> 
   <td colname="col3"> <p>Canto superior esquerdo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repetir= </span> </a> </p> </td> 
   <td colname="col2"> <p>Modo de repetição </p> </td> 
   <td colname="col3"> <p>0 (repetição direta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Nitidez </p> </td> 
   <td colname="col3"> <p>0 (sem nitidez). </p> </td> 
  </tr> 
 </tbody> 
</table>

Além desses atributos básicos, as texturas repetíveis são compatíveis com os seguintes atributos de finalidade especial para aplicativos avançados:

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> grout= </span> </a> </p> </td> 
   <td colname="col2"> <p>Cor e espessura da argamassa; útil para materiais de cerâmica/pedra </p> </td> 
   <td colname="col3"> <p>Grout já presente na imagem </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align= </span> </a> </p> </td> 
   <td colname="col2"> <p>Modo de alinhamento (entre objetos); usado para aplicações de estofamento </p> </td> 
   <td colname="col3"> <p>Correspondente ao centro </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotação= </span> </a> </p> </td> 
   <td colname="col2"> <p>Ângulo de rotação da textura; não suportado por objetos de parede </p> </td> 
   <td colname="col3"> <p>0 (sem rotação) </p> </td> 
  </tr> 
 </tbody> 
</table>
