---
description: Retorna 2 tipos diferentes de informações com base nos parâmetros passados. originatorHandle retorna informações sobre ativos gerados a partir do ativo especificado. generateHandle retorna informações sobre as etapas usadas para gerar o ativo ou arquivo especificado.
seo-description: Retorna 2 tipos diferentes de informações com base nos parâmetros passados. originatorHandle retorna informações sobre ativos gerados a partir do ativo especificado. generateHandle retorna informações sobre as etapas usadas para gerar o ativo ou arquivo especificado.
seo-title: getGenerationInfo
solution: Experience Manager
title: getGenerationInfo
topic: Dynamic Media Image Production System API
uuid: 4310a702-c08b-4479-9f57-9f2bc1d6b032
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# getGenerationInfo{#getgenerationinfo}

Retorna 2 tipos diferentes de informações com base nos parâmetros passados. originatorHandle retorna informações sobre ativos gerados a partir do ativo especificado. generateHandle retorna informações sobre as etapas usadas para gerar o ativo ou arquivo especificado.

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
| `*`Frase de código`*` | `xsd:string` | Sim | A alça da empresa. |
| `*`Frase de código`*` | `xsd:string` | Não | O mecanismo que foi usado na geração. Consulte Estilos de fonte. |
| `*`Frase de código`*` | `xsd:string` | Não | O identificador do ativo para query dos ativos gerados. |
| `*`Frase de código`*` | `xsd:string` | Não | O identificador do ativo para query de ativos e mecanismos usados em sua geração. |
| `*`Frase de código`*` | `xsd:StringArray` | Não | Propriedades incluídas na operação. |
| `*`Frase de código`*` | `xsd:StringArray` | Não | Propriedades excluídas da operação. |

**Saída (getGenerationInfoReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`GenerationArray`*` | `types:GenerationInfoArray` | Sim | Matriz de informações de geração. |

## Exemplos {#section-fdffe6ed82d94c7aa90e47f7ce889403}

Este exemplo de código retorna informações sobre ativos gerados a partir de um ativo específico. Ele não recupera informações sobre as etapas usadas para gerar o ativo especificado. A resposta é truncada para brevidade.

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

