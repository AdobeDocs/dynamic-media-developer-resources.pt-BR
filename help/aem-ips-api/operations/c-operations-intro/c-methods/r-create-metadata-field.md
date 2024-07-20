---
title: createMetadataField
description: Ele permite que os administradores criem campos de metadados para coordenar com sistemas de gerenciamento de conteúdo ou operações de modelo. Exemplos de campos de metadados criados incluem palavras-chave, informações sobre o autor da imagem ou informações sobre o detentor dos direitos autorais.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: eac7fa54-ebe2-4f42-a478-d9a6fb54d1b6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# createMetadataField{#createmetadatafield}

Ele permite que os administradores criem campos de metadados para coordenar com sistemas de gerenciamento de conteúdo ou operações de modelo. Exemplos de campos de metadados criados incluem palavras-chave, informações sobre o autor da imagem ou informações sobre o detentor dos direitos autorais.

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
   <td colname="col4"> O nome da empresa à qual o campo de metadados pertence. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Tipo de ativo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nome</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Nome do campo de metadados que você está criando. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4">Tipo de campo de metadados. <p>A constante de tipos de campo de metadados define os tipos disponíveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valorPadrão</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>O valor padrão do campo de metadados a ser criado (por exemplo, <span class="codeph"> Cena 7</span>). </p> <p>Os valores padrão não são compatíveis com tipos de campo de tag e devem ser omitidos. Se um padrão não vazio for especificado para um tipo de campo de tag, uma falha será retornada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Ocultar ou expor metadados específicos do sistema IPS. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname">isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Um sinalizador booleano que indica se o campo de metadados é aplicado (validado) quando o valor é definido. </p> <p>Se definido como verdadeiro, uma falha será gerada se um valor ilegal for definido em <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Ela permite criar um conjunto de valores específicos compartilhados para o qual as tags selecionadas podem apontar. </td> 
  </tr> 
 </tbody> 
</table>

**Saída (createMetadataFieldReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| fieldHandle | `xsd:string` | Sim | O identificador para o novo campo de metadados. |

## Exemplos {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

Esta amostra de código cria um campo de metadados do tipo string chamado `createMetadataField`. A resposta retorna o identificador para o novo campo de metadados.

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
