---
description: Retorna informações sobre a estrutura de uma empresa (número de arquivos, etc.).
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# getDiskUsage{#getdiskusage}

Retorna informações sobre a estrutura de uma empresa (número de arquivos, etc.).

## Tipos de usuário autorizados {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Entrada (getDiskUsageParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa cujo uso do disco você deseja obter. |

**Saída (getDiskUsageReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| diskUsageArray | `types:DiskUsageArray` | Sim | Matriz de uso de disco da empresa. |

## Exemplos {#section-cb16a97badc94076ad5da277db5ed16a}

O nome desta solicitação é enganoso. Em vez de retornar apenas um valor escalar que reflete o espaço em disco utilizado por uma empresa, ele obtém também outras informações sobre a estrutura de uma empresa.

**Solicitação**

```java
<ns1:getDiskUsageParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getDiskUsageParam>
```

**Resposta**

```java
<getDiskUsageReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <diskUsageArray>
      <items>
         <companyHandle>47</companyHandle>
         <companyName>My Company</companyName>
         <imageCount>207</imageCount>
         <diskSpaceUsage>3024</diskSpaceUsage>
         <lastModified>2007-09-14T22:10:30.661-07:00</lastModified>
      </items>
   </diskUsageArray>
</getDiskUsageReturn>
```
