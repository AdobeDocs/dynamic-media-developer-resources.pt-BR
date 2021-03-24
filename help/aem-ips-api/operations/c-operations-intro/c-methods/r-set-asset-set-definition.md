---
description: Atualiza a definição do conjunto de ativos existente.
solution: Experience Manager
title: setAssetSetDefinition
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---


# setAssetSetDefinition{#setassetsetdefinition}

Atualiza a definição do conjunto de ativos existente.

Sintaxe

## Tipos de usuário autorizados {#section-9d4ca3a8cfe74934b89971de01a2143c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-c2057a5a13d042c684a3da1b49bc5dc6}

**Entrada (setAssetDefinitionParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador para a empresa com o conjunto de ativos. |
| `*`assetHandle`*` | `xsd:string` | Sim | Identificador de conjunto de ativos |
| `*`setDefinition`*` | `xsd:string` | Sim | Sequência de definição. Veja abaixo. |

**Saída (setAssetSetDefinitionReturn)**

A API do IPS não retorna uma resposta para esta operação.

## parâmetro setDefinition: Sobre {#section-f88e066bf5294b4f8c12d5d652a5c94c}

**Funções setDefinition**

Especifique `setDefinition` funções de substituição em linha. Eles são resolvidos durante uma pesquisa de catálogo ou na publicação. As cadeias de caracteres de substituição têm o formato `${<substitution_func>}` e incluem o seguinte:

>[!NOTE]
>
>Os literais de tratamento nas listas de parâmetros devem ser cercados por colchetes `([])`. O texto fora de uma string de substituição é copiado para a string de saída durante a resolução.

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Função de Substituição </th> 
   <th colname="col2" class="entry"> Retorna o </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> Caminho do arquivo principal. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalogd([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> ID do catálogo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([  <span class="varname"> asset_handle  </span>],[  <span class="varname"> metadata_field_handle  </span>])  </span> </td> 
   <td colname="col2"> Valor dos metadados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> ID do catálogo. Aplica-se a ativos baseados em imagem (Imagem, Exibição ajustada, Exibição de camada). <p>Para outros ativos, retorna a ID de catálogo do ativo de ouro (se houver). Se nenhum ativo em miniatura estiver associado ao ativo, a função retornará uma string vazia. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplos de setDefinition**

Esta string de definição de conjunto de mídia:

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

Resolve o seguinte no momento da pesquisa ou publicação:

```java
jcompany/myRenderSet;jcompany/myRenderSet; 
1,jcompany/Videos/N08275_flv.flv;jcompany/myimg-1;2;20090703 10:05:53
```

## Exemplos {#section-739b42eec3074cafae285ec015a2d088}

**Solicitação**

```java
<setAssetSetDefinitionParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <assetHandle>a|1802|44|1802</assetHandle> 
   <setDefinition>${getCatalogId([a|1553|1|1176])};${getCatalogId([a|1553|1|1176])};1;img1, 
   ${getCatalogId([a|632|1|452])};${getCatalogId([a|632|1|452])};1,${getCatalogId([a|1664|22|1664])}; 
   ${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|1036|19|144])};${getCatalogId([ a|452|1|433])}; 
   2;${getMetadata([a1036|19|144], [m|1|ASSET|SharedDateField])}</setDefinition> 
</setAssetSetDefinitionParam>
```

**Resposta**

Nenhum.
