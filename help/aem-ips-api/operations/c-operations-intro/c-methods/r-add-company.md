---
description: Adiciona uma empresa ao sistema.
solution: Experience Manager
title: addCompany
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2f834fe8-a621-4a41-9473-8ef53294b348
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# addCompany{#addcompany}

Adiciona uma empresa ao sistema.

Envia o nome da empresa a ser adicionada ao sistema e, opcionalmente, envia se a empresa expira.

Quando essa operação é chamada, o sistema obtém um tipo companyInfo que contém um identificador de empresa e campos descritivos. Se o nome da empresa solicitado já existir no sistema, ele aciona um `ipsApiFault`.

## Tipos de usuário autorizados {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-c64a21b72585447880760db9e7a12ccb}

**Entrada (addCompanyParam)**

<table id="table_AA915BAD2E8E4A1B9719725994309CE8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obrigatório </p> </th> 
   <th colname="col4" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>O nome da empresa a adicionar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> expira</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:dateTime</span> </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>A data de vencimento da empresa. Forneça o fuso horário com a solicitação para esse campo. Os fusos horários são ajustados para a Hora central. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Saída (addCompanyReturn)**

<table id="table_89EBAC0E0FB34793BD843837BB02B518"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obrigatório </p> </th> 
   <th colname="col4" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Processe e nomeie, o caminho raiz, a data de expiração e a hora da nova empresa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplos {#section-4c8f1bb40d154c77a7b410468206e52b}

Este exemplo demonstra uma solicitação para adicionar uma empresa ao sistema IPS e a resposta detalhando as informações sobre a empresa adicionada necessárias para executar outras operações.

**Solicitação**

```java {.line-numbers}
<ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:addCompanyParam>
```

**Resposta**

```java {.line-numbers}
<ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:addCompanyReturn>
```
