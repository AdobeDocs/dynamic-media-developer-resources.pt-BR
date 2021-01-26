---
description: Define campos específicos de imagem para um ou mais ativos de imagem.
seo-description: Define campos específicos de imagem para um ou mais ativos de imagem.
seo-title: batchSetImageFields
solution: Experience Manager
title: batchSetImageFields
topic: Dynamic Media Image Production System API
uuid: e0ad7da4-cb28-4402-8b47-a600916d23b3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# batchSetImageFields{#batchsetimagefields}

Define campos específicos de imagem para um ou mais ativos de imagem.

Sintaxe

## Tipos de usuário autorizados {#section-6b087bdcb7874c13acf76e113a093054}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-4969815cf67c4d11b13bb2017b3604e8}

**Entrada (batchSetImageFields)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que contém os ativos de imagem. |
| `*`updateArray`*` | `types:ImageFieldUpdateArray` | Sim | A matriz do campo de imagem é atualizada. |

**Saída (batchSetImageFields)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sim | O número de campos de imagem definidos com êxito. |
| `*`warningCount`*` | `xsd:int` | Sim | O número de avisos gerados quando a operação tentou definir os campos de imagem. |
| `*`errorCount`*` | `xsd:int` | Sim | O número de erros gerados quando a operação tentou definir os campos de imagem. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram avisos quando a operação tentou aplicar as atualizações. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram erros quando a operação tentou aplicar as atualizações. |

## Exemplos {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

Este exemplo define dados nos campos de duas imagens em um storage de atualizações. Na matriz, as imagens são especificadas pelas alças do ativo e contêm resolução em pixels, coordenadas de âncora de posição x e y e dados do usuário. A resposta indica que os campos de ambas as imagens foram definidos com êxito.

**Solicitação**

```java
<batchSetImageFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|140626|1|102524</assetHandle>
         <resolution>72</resolution>
         <anchorX>50</anchorX>
         <anchorY>100</anchorY>
         <userData>nada1</userData>
      </items>
      <items>
         <assetHandle>a|96680|1|64865</assetHandle>
         <resolution>150</resolution>
         <anchorX>100</anchorX>
         <anchorY>50</anchorY>
         <userData>nada2</userData>
      </items>
   </updateArray>
</batchSetImageFieldsParam>
```

**Resposta**

```java
<batchSetImageFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetImageFieldsReturn>
```

