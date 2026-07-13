---
description: Define campos específicos de imagem para um ou mais ativos de imagem.
solution: Experience Manager
title: batchSetImageFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8ea6dbb8-4d32-43e5-961f-31110f983663
TQID: 'https://experienceleague.adobe.com/J3mCGBUY4Ws5Wq18tHWrHQJNElW5gYvwSQ2yKF-NhsM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 195
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
| companyHandle | `xsd:string` | Sim | O identificador da empresa que contém os ativos de imagem. |
| updateArray | `types:ImageFieldUpdateArray` | Sim | A matriz de atualizações de campo de imagem. |

**Saída (batchSetImageFields)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| successCount | `xsd:int` | Sim | O número de campos de imagem definidos com êxito. |
| warningCount | `xsd:int` | Sim | O número de avisos gerados quando a operação tentou definir os campos de imagem. |
| errorCount | `xsd:int` | Sim | O número de erros gerados quando a operação tentou definir os campos de imagem. |
| warningDetailArray | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram avisos quando a operação tentou aplicar as atualizações. |
| errorDetailArray | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram erros quando a operação tentou aplicar as atualizações. |

## Exemplos {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

Este exemplo define dados nos campos de duas imagens em uma matriz de atualização. Na matriz, as imagens são especificadas por seus identificadores de ativos e contêm a resolução em pixels, as coordenadas de âncora de posição x e y e os dados do usuário. A resposta indica que os campos de ambas as imagens foram definidos com êxito.

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

