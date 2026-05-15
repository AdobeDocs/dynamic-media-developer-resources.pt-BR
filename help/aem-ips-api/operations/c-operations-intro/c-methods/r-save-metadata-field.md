---
title: saveMetadataField
description: Criar ou editar um campo de metadados. Omita o identificador de campo opcional para criar um campo de metadados.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 56a45324-5027-4375-a790-c965f682e4b9
TQID: 'https://experienceleague.adobe.com/661cnE70CYiFh-uslg--BKP1ZzDxBr3wawnyqiRUuYk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 207
ht-degree: 0%

---

# saveMetadataField{#savemetadatafield}

Criar ou editar um campo de metadados. Omita o identificador de campo opcional para criar um campo de metadados.

>[!NOTE]
>
>Este método está obsoleto.

## Tipos de usuário autorizados {#section-0c1cbde0863346f8a31b32fd06ab2926}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-ec6827d485a143f4a059a92b18e40f4e}

**Entrada (saveMetadataFieldParam)**

<table id="table_C944A44352F2475A89CE86F3DB1B648A"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> O identificador da empresa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Identificador de campo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Escolha dos tipos de ativos dos quais os metadados serão salvos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nome</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Nome do campo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Escolha de tipos de campos de metadados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valorPadrão</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Valor padrão dos campos para todos os ativos. </td> 
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
 </tbody> 
</table>

**Saída (saveMetadataFieldReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| fieldHandle | `xsd:string` | Sim | Identificador do novo campo de metadados. |

## Exemplos {#section-4441c26d1f41466ba972b43dd5189e89}

Esta amostra de código cria um campo de metadados restrito pelas constantes de sequência Tipo de ativo e Tipos de campo de metadados. Se o elemento `fieldHandle` tiver um valor de identificador de campo válido, ele alterará os valores de metadados e obterá o mesmo identificador de campo especificado na solicitação.

**Solicitação**

```java
<ns1:saveMetadataFieldParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
   <ns1:name>Resolution</ns1:name>
   <ns1:fieldType>String</ns1:fieldType>
   <ns1:defaultValue>120</ns1:defaultValue>
</ns1:saveMetadataFieldParam>
```

**Resposta**

```java
<saveMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldHandle>47|ALL|Resolution</fieldHandle>
</saveMetadataFieldReturn>
```
