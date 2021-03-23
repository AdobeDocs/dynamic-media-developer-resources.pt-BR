---
description: Exclui um mapa de imagem.
seo-description: Exclui um mapa de imagem.
seo-title: deleteImageMap
solution: Experience Manager
title: deleteImageMap
uuid: 0abdf72c-f445-41d0-bd88-63b7ad1359d5
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# deleteImageMap{#deleteimagemap}

Exclui um mapa de imagem.

Sintaxe

## Tipos de usuário autorizados {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura e gravação ao ativo.

## Parâmetros {#section-28de12bab79045a5977c68855e37ae3d}

**Entrada (deleteImageMapParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que contém o mapa de imagem a ser excluído. |
| `*`imageMapHandle`*` | `xsd:string` | Sim | O identificador do mapa de imagem a ser excluído. |

**Saída (deleteImageMapParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

Essa amostra de código exclui um mapa de imagem de uma empresa. Você deve obter o identificador do mapa de imagem de outra operação.

**Solicitação**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Resposta**

Nenhum
