---
description: Dentro desse tipo, o campo pageReset é significativo para os tipos de ativo de imagem RenderSet e Catalog
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# [!DNL ImageSetMemberUpdate]{#imagesetmemberupdate}

Dentro desse tipo, o campo pageReset é significativo para os tipos de ativo de imagem RenderSet e Catalog:

* Para `RenderSet`, `pageReset` indica o início de um novo grupo de exibição/amostra de renderização.

* Para o Catálogo, `pageReset` indica o início de uma nova exibição de página. Normalmente, há duas imagens de página por exibição de página, mas você pode ter mais ou menos.

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Identificador de ativo na matriz do membro do conjunto de imagens. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3">Redefine a página. <p>A configuração é ignorada e o valor é forçado a true para <span class="codeph"> ImageSet</span> e <span class="codeph"> SpinSet</span>. </p></td> 
  </tr> 
 </tbody> 
</table>
