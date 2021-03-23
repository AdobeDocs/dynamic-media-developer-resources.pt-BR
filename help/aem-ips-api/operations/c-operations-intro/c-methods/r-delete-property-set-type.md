---
description: Exclui um tipo de conjunto de propriedades e seu conjunto de propriedades e propriedades associados.
seo-description: Exclui um tipo de conjunto de propriedades e seu conjunto de propriedades e propriedades associados.
seo-title: deletePropertySetType
solution: Experience Manager
title: deletePropertySetType
uuid: 7a5232cc-fa3a-4dac-bf88-8b954dd37c87
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# deletePropertySetType{#deletepropertysettype}

Exclui um tipo de conjunto de propriedades e seu conjunto de propriedades e propriedades associados.

Sintaxe

## Tipos de usuário autorizados {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-1c8973f5d35f44b4a6a483a41609e455}

**Entrada (deletePropertySetTypeParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Sim | O identificador do tipo de conjunto de propriedades a ser excluído. |

**Saída (deletePropertySetTypeParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-85faa2e3411a4e23aa6489037f7ce078}

Este exemplo de código usa o identificador do tipo como um campo no `deletePropertySetTypeParam` enviado ao servidor de serviços Web IPS para excluir o tipo de conjunto de propriedades.

**Solicitação**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Resposta**

Nenhum.
