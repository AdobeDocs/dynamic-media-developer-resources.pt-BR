---
title: SearchFilter
description: Filtros que ajudam você a definir critérios de pesquisa para tornar as pesquisas mais eficientes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b3a26966-33c9-48ca-b0ed-d05fc0e2050f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# [!DNL SearchFilter]{#searchfilter}

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
   <td colname="col3"> Especifique a pasta que deseja pesquisar. Deixe em branco para pesquisar toda a empresa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3">Defina como: 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> True</span>: pesquisar a pasta nomeada e todas as subpastas. </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> Falso</span>: para pesquisar somente a pasta nomeada. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipo:StringArray</span> </td> 
   <td colname="col3">Uma lista de tipos de ativos que você deseja retornar em uma pesquisa. Por exemplo, a <span class="codeph"> imagem</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipo:StringArray</span> </td> 
   <td colname="col3"> Especifique um tipo de ativo para excluir de uma pesquisa. Por exemplo, a imagem. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipo:StringArray</span> </td> 
   <td colname="col3">Uma lista de subtipos de ativos que você deseja retornar em uma pesquisa. Por exemplo, para um <span class="codeph"> AssetSet</span>, você pode pesquisar pelo subtipo <span class="codeph"> MediaType</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> strictSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Um sinalizador booleano opcional que especifica se os ativos sem subtipo devem ser retornados quando <span class="codeph"> assetSubTypeArray</span> for passado. </p> <p>Se verdadeiro, somente os ativos com um dos subtipos especificados serão retornados. </p> <p>Se false, os ativos sem subtipo também serão retornados. </p> <p>O padrão é falso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3">Defina como: 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> True</span>: retornar apenas ativos originais. </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> Falso</span>: Para retornar o conteúdo gerado. Por exemplo, imagens de um PDF carregado. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Processe o projeto que você deseja pesquisar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Especificar: 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E"><span class="codeph"> MarkedForPublish</span> para retornar apenas ativos publicados. </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672"><span class="codeph"> NotMarkedForPublish</span> para retornar apenas ativos não publicados. </li> 
    </ul> <p>Observação: deixe em branco para procurar por <i>todos</i> tipos de estado publicados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Especificar: 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48"><span class="codeph"> Qualquer</span> para retornar ativos independentemente do estado da lixeira. </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph"> NotInTrash</span> para retornar ativos 'normais'. </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6"><span class="codeph"> InTrash</span> para retornar ativos da lixeira. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
