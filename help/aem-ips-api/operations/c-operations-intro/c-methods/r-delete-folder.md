---
description: Exclui uma pasta.
seo-description: Exclui uma pasta.
seo-title: deleteFolder
solution: Experience Manager
title: deleteFolder
uuid: 76af65fb-86ef-43e2-bfec-3682acf0afe6
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# deleteFolder{#deletefolder}

Exclui uma pasta.

Sintaxe

## Tipos de usuário autorizados {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura e exclusão à pasta e a todos os seus filhos.

## Parâmetros {#section-a793c98a481a4f26ab50bc69b16b57e7}

**Entrada (deleteFolderParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa à qual a pasta pertence. |
| `*`folderHandle`*` | `xsd:string` | Sim | O identificador da pasta a ser excluída. |

**Saída (deleteFolderParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-9d4617b322e8442d80e59be0f8714841}

Esse código de amostra exclui uma pasta da raiz da empresa. Ele requer um identificador de pasta, que deve ser obtido de outra operação.

**Solicitação**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

Nenhum.
