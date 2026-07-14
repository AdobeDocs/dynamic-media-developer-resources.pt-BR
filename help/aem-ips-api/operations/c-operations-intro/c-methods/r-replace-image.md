---
description: Substitui os dados de imagem de um ativo de imagem.
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
TQID: 'https://experienceleague.adobe.com/11bWPLId2s4gOVhiIFr93Ca4D-7SJ0PYHFmiSKtStjk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 0%

---

# replaceImage{#replaceimage}

Substitui os dados de imagem de um ativo de imagem.

Sintaxe

## Tipos de usuário autorizados {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**Entrada (replaceImageParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyName | `xsd:string` | Sim | O identificador da empresa com a imagem que você deseja substituir. |
| assetHandle | `xsd:string` | Sim | O identificador do ativo que você deseja substituir. |
| urlModifier | `xsd:string` | Sim | Comandos do Servidor de imagens que geram novos dados de imagem. |

**Saída (replaceImageReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| assetHandle | `xsd:string` | Sim | Processe o novo ativo. |

## Exemplos {#section-cebb93576bde4cb98cb27356ca66783b}

Esta amostra de código substitui uma imagem e aplica um `urlModifier` com um comando que especifica que o Servidor de imagens não executa nenhuma ação na substituição.

**Solicitação**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**Resposta**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```

