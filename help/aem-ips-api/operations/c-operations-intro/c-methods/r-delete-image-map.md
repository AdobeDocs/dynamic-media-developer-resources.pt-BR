---
description: Exclui um mapa de imagem.
seo-description: Exclui um mapa de imagem.
seo-title: deleteImageMap
solution: Experience Manager
title: deleteImageMap
topic: Scene7 Image Production System API
uuid: 0abdf72c-f445-41d0-bd88-63b7ad1359d5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que contém o mapa de imagem a ser excluído. |
| ` *`imageMapHandle`*` | `xsd:string` | Sim | O identificador do mapa de imagem a ser excluído. |

**Saída (deleteImageMapParam)**

A API IPS não retorna uma resposta para esta operação.

## Exemplos {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

Esta amostra de código exclui um mapa de imagem de uma empresa. É necessário obter o identificador do mapa de imagem de outra operação.

**Solicitação**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Resposta**

Nenhum
