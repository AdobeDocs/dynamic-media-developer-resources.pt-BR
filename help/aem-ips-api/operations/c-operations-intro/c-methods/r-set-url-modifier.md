---
description: Define os comandos do protocolo Servidor de imagens ou Renderização de imagens para o ativo especificado. Esses comandos modificam a representação do ativo sem destruí-lo.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
TQID: 'https://experienceleague.adobe.com/dcz-gnw7NjHKN7EvsGvSRDmu4dgCUo2PPr3GjYLVoOA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 175
ht-degree: 0%

---

# setUrlModifier{#seturlmodifier}

Define os comandos do protocolo Servidor de imagens ou Renderização de imagens para o ativo especificado. Esses comandos modificam a representação do ativo sem destruí-lo.

Para o Servidor de imagens, os comandos no parâmetro `urlModifier` são publicados no campo de catálogo Modificador e aplicados antes de qualquer comando especificado na URL da solicitação. Os comandos em `urlPostApplyModifier` são publicados no campo de catálogo `PostModifier` e substituem quaisquer comandos na URL de solicitação ou em `urlModifier`. Para Renderização de Imagem, os comandos em `urlModifier` e `urlPostApplyModifier` são concatenados e publicados no campo de catálogo Modificador.

## Tipos de usuário autorizados {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Entrada (setUrlModifierParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | Identificador da empresa. |
| assetHandle | `xsd:string` | Sim | Identificador de ativo. |
| urlModifier | `xsd:string` | Não | Comandos do protocolo Image Serving ou Image Rendering a serem aplicados antes da solicitação ou `urlPostApplyModifier` comandos. |
| urlPostApplyModifier | `xsd:string` | Não | Comandos do protocolo Image Serving ou Image Rendering a serem aplicados após `urlModifier` e comandos request. |

**Saída (setUrlModifierReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-801d4b9b986443f59a5783a3d6bf44aa}

**Solicitação**

```java
<setUrlModifierParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|942|1|579</assetHandle>
   <urlModifier>modify=that</urlModifier>
   <urlPostApplyModifier>action=awesomeToo</urlPostApplyModifier>
</setUrlModifierParam>
```

**Resposta**

Nenhum.

