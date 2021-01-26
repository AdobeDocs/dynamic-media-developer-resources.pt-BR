---
description: 'Dentro desse tipo, o campo pageReset é significativo para os tipos de ativos de imagem RenderSet e Catalog '
seo-description: 'Dentro desse tipo, o campo pageReset é significativo para os tipos de ativos de imagem RenderSet e Catalog '
seo-title: ImageSetMemberUpdate
solution: Experience Manager
title: ImageSetMemberUpdate
topic: Dynamic Media Image Production System API
uuid: b0226d21-87ba-4e07-9819-79c9df3df13c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# ImageSetMemberUpdate{#imagesetmemberupdate}

Nesse tipo, o campo pageReset é significativo para os tipos de ativos de imagem RenderSet e Catalog:

* Para `RenderSet`, `pageReset` indica o start de uma nova visualização de renderização/grupo de amostras.

* Para Catálogo, `pageReset` indica o start de uma nova visualização de página. Geralmente, há 2 imagens de página por visualização de página, mas você pode ter mais ou menos.

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
   <td colname="col3"> Identificador de ativos na matriz de membros do conjunto de imagens. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3">Redefine a página. <p>A configuração é ignorada e o valor é forçado a true para <span class="codeph"> ImageSet</span> e <span class="codeph"> SpinSet</span>. </p></td> 
  </tr> 
 </tbody> 
</table>

