---
description: Exclui um grupo.
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# deleteGroup{#deletegroup}

Exclui um grupo.

Sintaxe

## Tipos de usuário autorizados {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-42775102ec724c36ae5241eea1a00b8e}

**Entrada (deleteGroupParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que pertence ao grupo que você deseja excluir. |
| `*`groupHandle`*` | `xsd:string` | Sim | O identificador do grupo que você deseja excluir. |

**Saída (deleteGroupParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-8f8501af3b3348a1b5701cf9622bf6e4}

Este código de amostra exclui um grupo de uma empresa. Requer um identificador de grupo, que deve ser obtido de outra operação.

**Solicitação**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**Resposta**

Nenhum.
