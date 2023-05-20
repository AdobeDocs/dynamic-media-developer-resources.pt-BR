---
description: Pesquise por ativos com base nos critérios especificados.
solution: Experience Manager
title: searchAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 58bd80e4-e9eb-43e4-8508-04e330f0ad26
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# searchAssets{#searchassets}

Pesquise por ativos com base nos critérios especificados.

Sintaxe

## searchAssets: Sobre {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` O é o principal método de recuperação de ativos de IPS. Esse método é usado para vários propósitos, como navegar na hierarquia de pastas ou encontrar um ativo específico por nome.

**Tamanho da resposta**

`searchAssets` retorna até 1000 ativos em uma única chamada. Para retornar até 10.000 ativos por chamada, limite os dados de resposta a um subconjunto de do `totalRows`, `name`, `handle`, `type`, e `subType` campos. Para retornar conjuntos maiores, configure a paginação com o `resultPage` parâmetro.

**Limitar Tamanho do Arquivo de Resultado com responseFieldArray ou excludeFieldArray**

Limite o tamanho do seu conjunto de dados com o `responseFieldArray` ou `excludFieldArray` parâmetros. Esses parâmetros ajudam a reduzir o uso de memória e a largura de banda e podem melhorar os tempos de resposta do servidor.

## Tipos de usuário autorizados {#section-9c4bc41bb8b4493982197eb13c7cdc55}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura para retornar ativos.

## Parâmetros {#section-49aabc0600764f55a8b7017d86ded44f}

**Entrada (searchAssetsParam)**

<table id="table_2972D1BB9CED4F7F9207747AE8CBAE8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obrigatório? </th> 
   <th colname="col4" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> O identificador da empresa com os ativos que você deseja pesquisar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Permite que os administradores trabalhem como um usuário diferente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Permite que os administradores trabalhem como parte de um grupo diferente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pasta</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> O caminho raiz para pesquisar por ativos. Se omitida, a pasta raiz da empresa será usada. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4">Defina como <span class="codeph"> true</span> para pesquisar subpastas. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Escolha de estado de publicação. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4">Opção de estado da lixeira. O padrão é <span class="codeph"> NotInTrash</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> conditionMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Escolha de Modos de Correspondência de Pesquisa para combinar resultados de <span class="codeph"> keywordArray</span>, </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span>, e <span class="codeph"> metadataConditionArray</span>. O padrão é <span class="codeph"> CorresponderTudo</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:MatrizDeCadeiaDeCaracteres</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p> <p>Observação: parâmetro obsoleto. Recomenda-se que você não o use. </p> </p> <p>Uma matriz de sequência de caracteres de palavras-chave a serem correspondidas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Escolha de Modos de Correspondência de Pesquisa para combinação <span class="codeph"> systemFieldCondition</span> corresponde. O padrão é <span class="codeph"> CorresponderTudo</span> </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipos:SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> A matriz de condições de campo do sistema. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4">Constantes de string dos Modos de correspondência de pesquisa. O padrão é <span class="codeph"> CorresponderTudo</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:TagConditionArray</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Uma matriz de predicados de pesquisa de campo de tag. </p> <p>Os predicados são combinados de acordo com a variável <span class="codeph"> tagMatchMode</span> e, em seguida, combinado com quaisquer termos no <span class="codeph"> keywordArray</span>, <span class="codeph"> systemFieldConditionArray</span>, e <span class="codeph"> metadataConditionArray</span> de acordo com a <span class="codeph"> conditionMatchMode</span> configuração. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4">Pesquisar Modos de Correspondência para combinação <span class="codeph"> metadataCondition</span> corresponde. O padrão é <span class="codeph"> CorresponderTudo</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipos:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> A matriz de condições de pesquisa de campo de metadados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:MatrizDeCadeiaDeCaracteres</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Matriz de tipos de ativos para incluir na pesquisa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:MatrizDeCadeiaDeCaracteres</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Matriz de tipos de ativos a serem excluídos da pesquisa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:MatrizDeCadeiaDeCaracteres</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Uma lista de nomes de subtipo para filtrar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4">Se <span class="codeph"> true</span> e <span class="codeph"> assetSubTypeArray</span> não estiver vazio, somente os ativos cujos subtipos estiverem em <span class="codeph"> assetSubTypeArray</span> são retornados. Se <span class="codeph"> false</span> (padrão), então os ativos sem subtipo definido são retornados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Se verdadeiro, os ativos de subprodutos gerados durante a assimilação de um ativo principal, como imagens de página de PDF copiadas, serão excluídos dos resultados da pesquisa. O padrão é falso. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludByproductArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipos:ExcludeByproductArray</span> </p> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Matriz de condições de geração de ativos de subprodutos a ser excluída dos resultados da pesquisa. Se presente, esse parâmetro substitui a configuração excludeByproducts. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Identificador de um projeto que contém os ativos a serem pesquisados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Número máximo de resultados a serem retornados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4">Especifica a página de resultados a ser retornada, com base em <span class="codeph"> recordsPerPage</span> tamanho da página. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Escolha dos campos de classificação de ativos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Escolha da direção da classificação. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:MatrizDeCadeiaDeCaracteres</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Contém uma lista de campos e subcampos para inclusão na resposta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:MatrizDeCadeiaDeCaracteres</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Contém uma lista de campos e subcampos a serem excluídos da resposta. </td> 
  </tr> 
 </tbody> 
</table>

**Saída (searchAssetsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| totalRows | `xsd:int` | Não | Número de linhas que uma pesquisa retorna quando os registros por página não são limitados. |
| assetArray | `types:AssetArray` | Não | Ativos retornados pela pesquisa. |

## Exemplos {#section-725484cc09b54772a838ad2cc930b94b}

Este exemplo de código pesquisa ativos de imagem que pertencem a uma empresa específica. A resposta é truncada por brevidade.

**Solicitação**

```java
<ns1:searchAssetsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeSubfolders>true</ns1:includeSubfolders>
   <ns1:assetTypeArray>
      <ns1:items>Image</ns1:items>
   </ns1:assetTypeArray>
</ns1:searchAssetsParam>
```

**Resposta**

```java
<searchAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <totalRows>210</totalRows>
   <assetArray>
      <items>
         <assetHandle>24265|1|17061</assetHandle>
         <type>Image</type>
         <name>Autumn Leaves</name>
         ...
      </items>
    </assetArray>
</searchAssetsReturn>
```
