---
description: Retorna 2 tipos diferentes de informações com base nos parâmetros transmitidos. originatorHandle retorna informações sobre ativos gerados a partir do ativo especificado. generateHandle retorna informações sobre as etapas usadas para gerar o ativo ou arquivo especificado.
seo-description: Retorna 2 tipos diferentes de informações com base nos parâmetros transmitidos. originatorHandle retorna informações sobre ativos gerados a partir do ativo especificado. generateHandle retorna informações sobre as etapas usadas para gerar o ativo ou arquivo especificado.
seo-title: getGenerationInfo
solution: Experience Manager
title: getGenerationInfo
uuid: 4310a702-c08b-4479-9f57-9f2bc1d6b032
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# getGenerationInfo{#getgenerationinfo}

Retorna 2 tipos diferentes de informações com base nos parâmetros transmitidos. originatorHandle retorna informações sobre ativos gerados a partir do ativo especificado. generateHandle retorna informações sobre as etapas usadas para gerar o ativo ou arquivo especificado.

Sintaxe

## Tipos de usuário autorizados {#section-9cc2216b32c74107be07aeacecc11401}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-b7fa94c82147455888e8469fa5f6922b}

**Entrada (getGenerationInfoParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`Frase do código`*` | `xsd:string` | Sim | O nome da empresa. |
| `*`Frase do código`*` | `xsd:string` | Não | O mecanismo usado na geração. Consulte Estilos de fonte. |
| `*`Frase do código`*` | `xsd:string` | Não | O identificador do ativo que será consultado para os ativos gerados. |
| `*`Frase do código`*` | `xsd:string` | Não | O identificador do ativo para consultar ativos e mecanismos usados em sua geração. |
| `*`Frase do código`*` | `xsd:StringArray` | Não | Propriedades incluídas na operação. |
| `*`Frase do código`*` | `xsd:StringArray` | Não | Propriedades excluídas da operação. |

**Saída (getGenerationInfoReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`generationArray`*` | `types:GenerationInfoArray` | Sim | Matriz de informações de geração. |

## Exemplos {#section-fdffe6ed82d94c7aa90e47f7ce889403}

Essa amostra de código retorna informações sobre ativos gerados a partir de um ativo específico. Ele não recupera informações sobre as etapas usadas para gerar o ativo especificado. A resposta é truncada por brevidade.

**Solicitação**

```java
<getGenerationInfoParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <originatorHandle>a|716|25|160</originatorHandle>
</getGenerationInfoParam>
```

**Resposta**

```java
<getGenerationInfoReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <generationArray>
      <items>
         <engine>PostScriptRip</engine>
         <originator>
         ...
         </generated>
         <attributeArray/>
      </items>
   </generationArray>
</getGenerationInfoReturn>
```

