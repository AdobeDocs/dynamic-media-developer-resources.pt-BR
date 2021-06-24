---
description: Retorna informações sobre a estrutura de uma empresa (número de arquivos, etc.).
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
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
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa cujo uso de disco você deseja obter. |

**Saída (getDiskUsageReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`diskUsageArray`*` | `types:DiskUsageArray` | Sim | Matriz de uso de disco da empresa. |

## Exemplos {#section-cb16a97badc94076ad5da277db5ed16a}

O nome deste pedido é enganador. Em vez de retornar apenas um valor escalar que reflete quanto espaço em disco uma empresa está usando, ela também recebe outras informações sobre a estrutura de uma empresa.

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
