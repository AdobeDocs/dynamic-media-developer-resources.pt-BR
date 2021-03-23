---
description: Pesquisa o repositório de índice de metadados para os termos de pesquisa fornecidos. Retorna dados do ativo como o método searchAssets.
seo-description: Pesquisa o repositório de índice de metadados para os termos de pesquisa fornecidos. Retorna dados do ativo como o método searchAssets.
seo-title: searchAssetsByMetadata
solution: Experience Manager
title: searchAssetsByMetadata
uuid: f4119ee9-f6d8-49fb-9d8c-bb200951d983
feature: Dynamic Media Classic, SDK/API, metadados, gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---


# searchAssetsByMetadata{#searchassetsbymetadata}

Pesquisa o repositório de índice de metadados para os termos de pesquisa fornecidos. Retorna dados do ativo como o método searchAssets.

Embora `searchAssetsByMetadata` permita pesquisar em Campos de Metadados Definidos pelo Usuário, esses campos não serão retornados se forem especificados em `responseMetadataArray`. Para ilustrar esse ponto, o seguinte exemplo de código:

```java
<ns:responseMetadataArray>
 <ns:items>custom_attributes.x</ns:items>
</ns:responseMetadataArray>
```

retorna um valor nulo:

```java
<items>
 <name>custom_attributes.x</name>
 <value>null</value>
</items>
```

Para contornar esse problema, você pode usar o `fieldHandles` dos ativos retornados da pesquisa para executar `getAssets` (consulte também [getAssets](../../../operations/c-operations-intro/c-methods/r-get-assets.md#reference-adad4f504f684d3dabc09e093b8511ca)). Esse método obtém os valores de Campos Definidos pelo Usuário para os ativos em questão. Use o exemplo de sintaxe a seguir para pesquisar em Campos de Metadados Definidos pelo Usuário:

```java
<ns:metadataConditionArray>
 <ns:items>
  <ns:fieldHandle>custom_attributes.[UDF Field Name]</ns:fieldHandle>
  <ns:op>[Conditional]</ns:op>
  <ns:value>[Value]</ns:value>
 </ns:items>
</ns:metadataConditionArray>
```

## Tipos de usuário autorizados {#section-9f85dd55ab574104b5fdc0f95aa0a0e2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-5f1edb9c5b914160ab361f4364b8aa8d}

**Entrada (searchAssetsByMetadataParam)**

<table id="table_8FF228D6279241849F3D9E5BA080580C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obrigatório </th> 
   <th colname="col4" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>O nome da empresa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> Filtro</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipo:SearchFilter</span> </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Filtros que ajudam você a definir critérios de pesquisa. </p> <p>Consulte <a href="../../../types/c-data-types/r-search-filter.md#reference-0e2eb87bccae4b69be6717267bcb80aa" format="dita" scope="local"> SearchFilter</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipo:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Condições que definem critérios de pesquisa. Consulte abaixo para obter mais informações. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> responseMetadataArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Campos adicionais que você deseja que tenham preenchido na resposta no resumo do ativo. Os campos devem ser especificados no formato normalizado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>O número de ativos retornados pela resposta. O valor padrão é 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Especifica a página de resultados a ser retornada, com base no tamanho da página <span class="codeph"> recordsPerPage</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> sortBy</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Classificar por campo de ativo selecionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> sortDirection</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Escolha de uma espécie de direção. Crescente é padrão. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Saída (searchAssetsByMetadataReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`totalRows`*` | `xsd:int` | Não | Número de correspondências. |
| `*`assetArray`*` | `types:AssetArray` | Não | Matriz de ativos retornados pela pesquisa. |

## Detalhes de metadataConditionArray {#section-1af4a4a22f82451eabdf6dfe13d9f27d}

**Estrutura do item**

`metadataConditionArray` A estrutura é a seguinte:

```java
<ns1:items>
   <ns:fieldHandle>field_handle</ns:fieldHandle>
   <ns:op>operator</ns:op>
   <ns:value>comparison_value</ns:value>
</ms1:items>
```

**Valores**

`field_handle` é a chave de pesquisa de metadados. Ele pode conter notação de pontos. Os valores possíveis incluem:

* `asset_id` (sem prefixo)
* `name`
* `folder_path`
* `type`
* `file_name`
* `description`
* `comment`
* `user_data`
* `sku`
* `modified_at`
* `modified_by`
* `created_at` (Igual a  `modified_at` (Data no formulário: 08 de julho de 2014 22:13:45 GMT-0500 (CDT)

* `created_by`

**Operadores permitidos**

O [!DNL operator] define como comparar o valor e incluir:

* `Equals`
* `NotEquals`
* `Contains`
* `NotContains`
* `StartsWith`
* `EndsWith`

O `comparison_value` é o termo a ser procurado.

## Exemplos {#section-53a12b9c023e4e629eddf5719c955ad4}

Essa amostra de código realiza uma pesquisa com os seguintes critérios de metadados:

* `name` contém  `1000801`.

* `dc.rights` campo é igual a  `Per Jessen Schmidt`.

**Solicitação**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
          <xsd:user>user@adobe.com</xsd:user>
          <xsd:password>topSecret</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
      <ns:searchAssetsByMetadataParam>
         <ns:companyHandle>c|656</ns:companyHandle>
         <ns:metadataConditionArray>
            <ns:items>
               <ns:fieldHandle>name</ns:fieldHandle>
               <ns:op>Contains</ns:op>
               <ns:value>1000801</ns:value>
            </ns:items>
            <ns:items>
               <ns:fieldHandle>dc.rights</ns:fieldHandle>
               <ns:op>Equals</ns:op>
               <ns:value>Per Jessen Schmidt</ns:value>
            </ns:items>
         </ns:metadataConditionArray>
         <ns:responseMetadataArray>
            <ns:items>dc.subject</ns:items>
            <ns:items>xmp.CreatorTool</ns:items>
         </ns:responseMetadataArray>
      </ns:searchAssetsByMetadataParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**Resposta**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <searchAssetsByMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <totalRows>1</totalRows>
         <assetSummaryArray>
            <items>
               <assetHandle>a|885289</assetHandle>
               <type>Image</type>
               <name>test9-1000801</name>
               <folder>Extroscope/Test subfolders/</folder>
               <filename>test9-1000801.jpg</filename>
               <created>2009-11-19T07:21:24.252-08:00</created>
               <createUser>pschmidt@adobe.com</createUser>
               <lastModified>2009-11-19T07:21:25.487-08:00</lastModified>
               <lastModifyUser>pschmidt@adobe.com</lastModifyUser>
               <metadataArray>
                  <items>
                     <name>dc.subject</name>
                     <value>[San Fransico, USA</value>
                  </items>
                  <items>
                     <name>xmp.CreatorTool</name>
                     <value>Ver.1.0</value>
                  </items>
               </metadataArray>
            </items>
         </assetSummaryArray>
      </searchAssetsByMetadataReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

