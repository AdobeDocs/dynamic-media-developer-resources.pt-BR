---
description: Exclui um mapa de imagem.
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
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
| companyHandle | `xsd:string` | Sim | O identificador da empresa que contém o mapa de imagem a ser excluído. |
| imageMapHandle | `xsd:string` | Sim | O identificador do mapa de imagem a ser excluído. |

**Saída (deleteImageMapParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

Esta amostra de código exclui um mapa de imagem de uma empresa. Você deve obter o identificador de mapa de imagem de outra operação.

**Solicitação**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Resposta**

Nenhum
