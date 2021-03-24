---
description: Restaura ativos da lixeira.
solution: Experience Manager
title: restoreAssetsFromTrash
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---


# restoreAssetsFromTrash{#restoreassetsfromtrash}

Restaura ativos da lixeira.

Sintaxe

## Tipos de usuário autorizados {#section-15e887782c7d4ace897ff02c6ad5baa0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-200a61d040c94e489a85241b29cd499a}

**Entrada (restoreAssetsFromTrashParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O controle de uma empresa com os ativos que você deseja restaurar. |
| `*`assetHandleArray`*` | `types:HandleArray` | Sim | Matriz de manipuladores para os ativos que você deseja restaurar. |

**Saída (restoreAssetsFromTrashReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sim | Número de ativos removidos da lixeira com êxito. |
| `*`warningCount`*` | `xsd:int` | Sim | Número de avisos gerados quando a operação tentou restaurar ativos da lixeira. |
| `*`errorCount`*` | `xsd:int` | Sim | Número de erros gerados ao tentar restaurar ativos da lixeira. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram avisos quando a operação tentou restaurar ativos da lixeira. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram erros quando a operação tentou restaurar ativos da lixeira. |

## Exemplos {#section-98fe0394b0634ca397c395f14f8a9358}

Essa amostra de código restaura ativos da lixeira. A resposta indica que a operação foi concluída com êxito.

**Solicitação**

```java
<restoreAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</restoreAssetsFromTrashParam>
```

**Resposta**

```java
<restoreAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</restoreAssetsFromTrashReturn
```

