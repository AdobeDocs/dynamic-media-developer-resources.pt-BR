---
description: Permite que os administradores criem novos campos de metadados para coordenar com sistemas de gerenciamento de conteúdo ou para operações de modelo. Exemplos de campos de metadados criados incluem palavras-chave, informações sobre o autor da imagem ou informações do detentor dos direitos autorais.
seo-description: Permite que os administradores criem novos campos de metadados para coordenar com sistemas de gerenciamento de conteúdo ou para operações de modelo. Exemplos de campos de metadados criados incluem palavras-chave, informações sobre o autor da imagem ou informações do detentor dos direitos autorais.
seo-title: createMetadataField
solution: Experience Manager
title: createMetadataField
uuid: 50ab61fa-df44-4305-ad9f-693c4aea1e69
feature: Dynamic Media Classic, SDK/API, Metadados
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# createMetadataField{#createmetadatafield}

Permite que os administradores criem novos campos de metadados para coordenar com sistemas de gerenciamento de conteúdo ou para operações de modelo. Exemplos de campos de metadados criados incluem palavras-chave, informações sobre o autor da imagem ou informações do detentor dos direitos autorais.

Sintaxe

## Tipos de usuário autorizados {#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## Parâmetros {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**Entrada (createMetadataFieldParam)**

<table id="table_E5B249BBED3B4D2F9CEE2CCF27472D1B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome do parâmetro </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obrigatório </th> 
   <th colname="col4" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Nome da empresa à qual o campo de metadados pertence. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Tipo de ativo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Nome do campo de metadados que você está criando. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4">Tipo de campo de metadados. <p>A constante de tipos de campos de metadados define os tipos disponíveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>O valor padrão do campo de metadados a ser criado (por exemplo, <span class="codeph"> Scene7</span>). </p> <p>Valores padrão não são suportados para tipos de campos de tag e devem ser omitidos. Se um padrão que não esteja vazio for especificado para um tipo de campo de tag, uma falha será retornada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Ocultar ou expor os metadados específicos do sistema IPS. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Um sinalizador booleano que indica se o campo de metadados é aplicado (validado) quando o valor é definido. </p> <p>Se definido como true, uma falha será lançada se um valor inválido for definido em <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Permite criar um conjunto de valores enumerados compartilhados para os quais as tags selecionadas podem apontar. </td> 
  </tr> 
 </tbody> 
</table>

**Saída (createMetadataFieldReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`fieldHandle`*` | `xsd:string` | Sim | O identificador do novo campo de metadados. |

## Exemplos {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

Essa amostra de código cria um campo de metadados do tipo string chamado `createMetadataField`. A resposta retorna o identificador para o novo campo de metadados.

**Solicitação**

```java
<createMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetType>Image</assetType>
   <name>createMetadataField</name>
   <fieldType>String</fieldType>
   <initialTagValue>Fall</initialTagValue>
   <defaultValue>Default</defaultValue>
</createMetadataFieldParam>
```

**Resposta**

```java
<createMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
</createMetadataFieldReturn>
```

