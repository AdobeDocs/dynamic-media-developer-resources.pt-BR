---
title: createAssetSet
description: Cria um conjunto de ativos genérico com uma cadeia de caracteres de definição de conjunto bruto a ser publicada em um Servidor de imagens.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 4565eb4f-eeb7-4b98-bfef-1a59e9a931af
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# createAssetSet{#createassetset}

Cria um conjunto de ativos genérico com uma cadeia de caracteres de definição de conjunto bruto a ser publicada em um Servidor de imagens.

Sintaxe

## Tipos de usuário autorizados {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-3580b586296e42a5b21426085b1bb72d}

**Entrada (createAssetSet)**

<table id="table_2C70C33A127242FC828FCD8EC852E1EC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> O identificador da empresa que contém o conjunto de ativos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> O identificador da pasta na qual o novo conjunto de ativos é criado. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nome </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Nome do ativo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subtipo </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Um identificador exclusivo criado pelo cliente para o tipo de conjunto de ativos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Os parâmetros na cadeia de caracteres de definição do conjunto. <p>Esses parâmetros devem ser resolvidos para o formato especificado pelo visualizador de destino. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Identificador do ativo que atua como a miniatura do novo conjunto de imagens. Se não for especificado, o IPS tentará usar o primeiro ativo de imagem referenciado pelo conjunto. </td> 
  </tr> 
 </tbody> 
</table>

**Funções de Substituição para setDefinition**

Você pode especificar funções de substituição em linha que são resolvidas durante a pesquisa de catálogo ou publicação. Cadeias de substituição têm o formato `${<substitution_func>}`. As funções disponíveis são descritas abaixo.

>[!NOTE]
>
>Os literais de identificador em listas de parâmetros devem estar entre colchetes `([])`. Todo o texto que está fora de uma cadeia de caracteres de substituição é copiado textualmente para a cadeia de caracteres de saída durante a resolução.

| **Função de Substituição** | **Devoluções** |
|---|---|
| `getFilePath([asset_handle>])` | O caminho do arquivo de origem principal do ativo. |
| `getCatalogId([<asset_handle>])` | A ID do catálogo do ativo. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | Valores de metadados para o ativo. |
| `getThumbCatalogId([<asset_handle>])` | A ID do catálogo do ativo (somente para ativos baseados em imagem). A ID de catálogo do ativo de miniatura associado (para outros ativos). Se um ativo de miniatura associado não estiver disponível, a função retornará uma cadeia de caracteres vazia. |

**Exemplo de cadeia de caracteres de definição de conjunto de mídia**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

Na pesquisa de catálogo ou no momento da publicação, esse processo é resolvido como uma cadeia de caracteres semelhante à seguinte:

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**Saída (createAssetSet)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| assetHandle | `xsd:string` | Sim | O identificador do conjunto de ativos. |

## Exemplos {#section-fed53089de824d67ab96cd9103d384b4}

**Solicitação**

```java
<createAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <folderHandle>f|jcompany/AssetSets/</folderHandle> 
   <name>testAssetSet</name> 
   <subType>MediaSet</subType> 
</createAssetSetParam>
```

**Resposta**

```java
<createAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <assetHandle>a|1801|44|1801</assetHandle> 
</createAssetSetReturn>
```
