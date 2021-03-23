---
description: Retorna informações sobre a estrutura de uma empresa (número de arquivos, etc.).
seo-description: Retorna informações sobre a estrutura de uma empresa (número de arquivos, etc.).
seo-title: getDiskUsage
solution: Experience Manager
title: getDiskUsage
uuid: 29190200-8f49-4689-9782-1df665dca1b7
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '116'
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

