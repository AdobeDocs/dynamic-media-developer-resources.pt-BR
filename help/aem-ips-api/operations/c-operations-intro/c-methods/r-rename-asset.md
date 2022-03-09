---
description: Renomeia um ativo.
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# renameAsset{#renameasset}

Renomeia um ativo.

>[!NOTE]
>
>O `renameFiles` foi descontinuado para versões anteriores e removido de `renameAsset`. O caminho do arquivo virtual é alterado para corresponder ao novo nome do ativo (preservando a extensão do arquivo), enquanto os caminhos de arquivo físico não são afetados. Os clientes da API precisam remover referências a esse parâmetro ao atualizar para a nova versão da API.

## Tipos de usuário autorizados {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura e gravação ao ativo.

## Parâmetros {#section-ef95a994106841e0ab346dd4cf672258}

**Entrada (renameAssetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa à qual o ativo pertence. |
| assetHandle | `xsd:string` | Sim | O identificador do ativo que deseja renomear. |
| newName | `xsd:string` | Sim | Novo nome do ativo. |
| validateName | `xsd:boolean` | Sim | Se a variável `validateName` é `true` e o tipo de ativo requer uma ID IPS exclusiva, então o novo nome é verificado para fins de exclusividade global e `renameAsset` gera uma falha se não for exclusiva. |

**Saída (renameAssetReturn)**

A API do IPS não retorna uma resposta para esta operação. Consulte a descrição do `<ns1:validateName>` para avisos sobre esse elemento.

## Exemplos {#section-a0ddffd62bec42e09069f22ceb486f8a}

Essa amostra de código renomeia um ativo

**Solicitação**

```java
<ns1:renameAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:newName>My Newly Renamed Image</ns1:newName>
   <ns1:validateName>true</ns1:validateName>
   <ns1:renameFiles>true</ns1:renameFiles>
</ns1:renameAssetParam>
```

**Resposta**

Nenhum.
