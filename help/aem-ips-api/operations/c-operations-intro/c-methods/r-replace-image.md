---
description: Substitui os dados da imagem de um ativo de imagem.
seo-description: Substitui os dados da imagem de um ativo de imagem.
seo-title: replaceImage
solution: Experience Manager
title: replaceImage
topic: Dynamic Media Image Production System API
uuid: 46824e33-265c-4425-9ab1-8ad6b7ac154d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---


# replaceImage{#replaceimage}

Substitui os dados da imagem de um ativo de imagem.

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
| `*`companyName`*` | `xsd:string` | Sim | A alça da empresa com a imagem que você deseja substituir. |
| `*`assetHandle`*` | `xsd:string` | Sim | O identificador do ativo que você deseja substituir. |
| `*`urlModifier`*` | `xsd:string` | Sim | Comandos do Servidor de imagens que geram novos dados de imagem. |

**Saída (replaceImageReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Sim | Lidar com o novo ativo. |

## Exemplos {#section-cebb93576bde4cb98cb27356ca66783b}

Essa amostra de código substitui uma imagem e aplica um `urlModifier` com um comando que especifica que o Servidor de imagens não executará nenhuma ação após a substituição.

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

