---
description: Filtros que ajudam você a definir critérios de pesquisa para tornar as pesquisas mais eficientes.
seo-description: Filtros que ajudam você a definir critérios de pesquisa para tornar as pesquisas mais eficientes.
seo-title: SearchFilter
solution: Experience Manager
title: SearchFilter
topic: Dynamic Media Image Production System API
uuid: 85a434d3-51a5-4e68-901e-70585c0e8b20
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# SearchFilter{#searchfilter}

Filtros que ajudam você a definir critérios de pesquisa para tornar as pesquisas mais eficientes.

Sintaxe

## Parâmetros {#section-4c611d9bbe0d418d882632605fc4d29d}

<table id="table_57CEE262A33A4E898C6AFB30C93FD874"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pasta</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Especifique a pasta que deseja pesquisar. Deixe em branco para pesquisar por toda a empresa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3">Definir como: 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> Verdadeiro</span>: Para pesquisar a pasta nomeada e todas as subpastas. </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> Falso</span>: Para pesquisar somente a pasta nomeada. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">Uma lista de tipos de ativos que você deseja retornar em uma pesquisa. Por exemplo, <span class="codeph"> image</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3"> Especifique um tipo de ativo a ser excluído de uma pesquisa. Por exemplo, imagem. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">Uma lista de subtipos de ativos que você deseja retornar em uma pesquisa. Por exemplo, para um AssetSet <span class="codeph"></span>, você pode pesquisar pelo subtipo <span class="codeph"> MediaType</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> hardSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Um sinalizador booleano opcional que especifica se os ativos devem ser retornados sem subtipo quando <span class="codeph"> assetSubTypeArray</span> for transmitido. </p> <p>Se verdadeiro, somente os ativos com um dos subtipos especificados serão retornados. </p> <p>Se falso, os ativos sem subtipo também serão retornados. </p> <p>Os padrões são falsos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3">Definir como: 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> Verdadeiro</span>: Para retornar somente ativos originais. </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> Falso</span>: Para retornar o conteúdo gerado. Por exemplo, imagens de um PDF carregado. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Manipule o projeto que deseja pesquisar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Especificar: 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E"><span class="codeph"> </span> MarkedForPublishto retorna somente ativos publicados. </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672"><span class="codeph"> </span> NotMarkedForPublishto retorna somente ativos não publicados. </li> 
    </ul> <p>Observação: Deixe em branco para pesquisar por <i>todos</i> tipos de estado publicados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Especificar: 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48"><span class="codeph"> </span> Qualquer pessoa que retorna ativos independentemente do estado de lixo. </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph"> </span> NotInTrashto retorna ativos "normais". </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6"><span class="codeph"> O </span> InTrashto retorna ativos do lixo. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

