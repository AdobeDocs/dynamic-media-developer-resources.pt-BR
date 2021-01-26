---
description: Define valores de metadados para um ativo específico usado com setAssetMetadata. Descreve as alterações que você deseja fazer nos metadados.
seo-description: Define valores de metadados para um ativo específico usado com setAssetMetadata. Descreve as alterações que você deseja fazer nos metadados.
seo-title: MetadataUpdate
solution: Experience Manager
title: MetadataUpdate
topic: Dynamic Media Image Production System API
uuid: 09d3940b-117d-4d83-8b12-e86520c9da34
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---


# MetadataUpdate{#metadataupdate}

Define valores de metadados para um ativo específico usado com setAssetMetadata. Descreve as alterações que você deseja fazer nos metadados.

>[!NOTE]
>
>Se o campo de valor único for transmitido, o valor da tag do ativo será redefinido para o valor da tag especificado.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Identificador de campo de metadados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Valor de atualização de metadados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> Valor de metadados booleanos (somente para campos digitados como booleanos). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Valor de metadados longos (somente para campos sem tipo). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:duplo</span> </td> 
   <td colname="col3"> Valor dos metadados do duplo (somente para campos de tipo flutuante). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Valor de metadados de data (somente para campos digitados por data). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> addTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> <p>Adiciona à lista de valor de tag existente para o ativo. 
     <ul id="ul_08DE6C490B614560A6118E7AC59720E3"> 
      <li id="li_358A3BDC0EC94CCF8178CD789F09F804">Campos de tag de valor único armazenam somente o último valor. </li> 
      <li id="li_3F47D3A3C63A4752BF9A45F7B00A6E70">Um campo de tag de dicionário fixo retornará uma falha se o valor não estiver no dicionário. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3">Substitui a lista de valor de tag existente para o ativo. 
    <ul id="ul_941C915C69E84CF2AC5938378837EB92"> 
     <li id="li_6E85019335034B2EB1302696AE690ED5">Campos de tag de valor único armazenam somente o último valor. </li> 
     <li id="li_0DC56717EBB642D29FB7A3D043CEDED1">Um campo de tag de dicionário fixo retornará uma falha se o valor não estiver no dicionário. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> deleteTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> Exclui os valores especificados da lista de valor de tag do ativo, se houver. </td> 
  </tr> 
 </tbody> 
</table>

