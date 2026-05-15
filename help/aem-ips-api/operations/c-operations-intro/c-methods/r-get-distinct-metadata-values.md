---
description: Retorna todos os valores de um campo de metadados.
solution: Experience Manager
title: getDistinctMetadataValue
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 1987d8b0-64e4-49be-af45-98e4c6542e5f
TQID: https://experienceleague.adobe.com/k5qqGZml4RAzJ2UCgtsIbI0dpxwYnl1561znBOgBrv8
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 0f5947b3f28ba40cd479df463c843f7e99155d5e
workflow-type: tm+mt
source-wordcount: 65
ht-degree: 0%

---

# getDistinctMetadataValue{#getdistinctmetadatavalues}

Retorna todos os valores de um campo de metadados.

Sintaxe

## Tipos de usuário autorizados {#section-f0f44fdcb318490582dd04de8eaf745d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-600f36a32ff147cb83149943d37843e2}

**Entrada (getDistinctMetadataValuesParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa para a qual você deseja obter dados. |
| metadataKey | `xsd:string` | Sim | Chave de metadados na notação de pontos. |

**Saída (getDistinctMetadataValuesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| valueArray | `types:ValueArray` | Sim | Valores do campo de metadados solicitado. |

## Exemplos {#section-0189fa6fb31646cda5ce1b0bc4fcdf46}

**Solicitação**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
         <xsd:user>user@company.com</xsd:user>
         <xsd:password>password</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
   <ns:getDistinctMetadataValuesParam>
      <ns:companyHandle>680</ns:companyHandle>
      <ns:metadataKey>dc.format</ns:metadataKey>
      </ns:getDistinctMetadataValuesParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**Resposta**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <getDistinctMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <valueArray>
            <items>
               <value>N/A</value>
               <count>412</count>
            </items>
            <items>
               <value>image/jpeg</value>
               <count>189</count>
            </items>
            <items>
               <value>image/epsf</value>
               <count>1</count>
            </items>
            <items>
               <value>image/tiff</value>
               <count>3</count>
            </items>
         </valueArray>
      </getDistinctMetadataValuesReturn>
   </soapenv:Body>
</soapenv:Envelope>
```
