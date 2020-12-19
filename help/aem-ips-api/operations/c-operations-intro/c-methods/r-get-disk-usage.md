---
description: Retorna informações sobre uma estrutura de empresa (número de arquivos, etc.).
seo-description: Retorna informações sobre uma estrutura de empresa (número de arquivos, etc.).
seo-title: getDiskUsage
solution: Experience Manager
title: getDiskUsage
topic: Scene7 Image Production System API
uuid: 29190200-8f49-4689-9782-1df665dca1b7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# getDiskUsage{#getdiskusage}

Retorna informações sobre uma estrutura de empresa (número de arquivos, etc.).

## Tipos de usuário autorizados {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Entrada (getDiskUsageParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa cujo uso de disco você deseja obter. |

**Saída (getDiskUsageReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`diskUsageArray`*` | `types:DiskUsageArray` | Sim | Matriz de uso do disco de empresa. |

## Exemplos {#section-cb16a97badc94076ad5da277db5ed16a}

O nome deste pedido é enganoso. Em vez de retornar apenas um valor escalar que reflete a quantidade de espaço em disco que uma empresa está usando, ele também recebe outras informações sobre a estrutura de uma empresa.

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

