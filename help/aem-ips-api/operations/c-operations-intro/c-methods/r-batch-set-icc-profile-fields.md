---
description: Define campos de metadados de perfil ICC.
seo-description: Define campos de metadados de perfil ICC.
seo-title: batchSetIccProfileFields
solution: Experience Manager
title: batchSetIccProfileFields
topic: Scene7 Image Production System API
uuid: 163b9b36-85b6-4880-8029-8421b04f4a08
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# batchSetIccProfileFields{#batchseticcprofilefields}

Define campos de metadados de perfil ICC.

Sintaxe

## Tipos de usuário autorizados {#section-f6f7caf9434b4f469518dab64b76c0f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-75a02b55ae0d444ca26b59aac6e86d6f}

**Entrada (batchSetIccProfileFields)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sim | Manuseie a empresa que contém os perfis ICC. |
| ` *`matriz de atualização`*` | `xsd:string` | Sim | Matriz de atualizações de perfis ICC. |

**Saída (batchSetIccProfileFields)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Sim | O número de campos de perfil ICC definidos com êxito. |
| ` *`warningCount`*` | `xsd:int` | Sim | O número de avisos gerados quando a operação tentou definir os campos de perfil ICC. |
| ` *`errorCount`*` | `xsd:int` | Sim | O número de erros gerados quando a operação tentou definir os campos do perfil ICC. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram avisos quando a operação tentou aplicar as atualizações. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram erros quando a operação tentou aplicar as atualizações. |

## Exemplos {#section-5dc90cfbd9b1411485b44859032f7cb9}

**Solicitação**

```java
<batchSetIccProfileFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|1808|13|169</assetHandle>
         <class>Output</class>
         <colorSpace>CMYK</colorSpace>
         <pcsType>Luv</pcsType>
      </items>
   </updateArray>
</batchSetIccProfileFieldsParam>
```

**Resposta**

```java
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```

