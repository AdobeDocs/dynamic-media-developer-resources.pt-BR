---
description: Retorna dois tipos diferentes de informações com base nos parâmetros transmitidos. originatorHandle retorna informações sobre ativos gerados a partir do ativo especificado. generateHandle retorna informações sobre etapas usadas para gerar o ativo ou arquivo especificado.
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# getGenerationInfo{#getgenerationinfo}

Retorna dois tipos diferentes de informações com base nos parâmetros transmitidos. originatorHandle retorna informações sobre ativos gerados a partir do ativo especificado. generateHandle retorna informações sobre etapas usadas para gerar o ativo ou arquivo especificado.

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
| Frase de código | `xsd:string` | Sim | O identificador da empresa. |
| Frase de código | `xsd:string` | Não | O mecanismo que foi usado na geração. Consulte Estilos de fonte. |
| Frase de código | `xsd:string` | Não | O identificador do ativo para consultar por ativos gerados. |
| Frase de código | `xsd:string` | Não | O identificador do ativo para consultar ativos e mecanismos usados em sua geração. |
| Frase de código | `xsd:StringArray` | Não | Propriedades incluídas na operação. |
| Frase de código | `xsd:StringArray` | Não | Propriedades excluídas da operação. |

**Saída (getGenerationInfoReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| generationArray | `types:GenerationInfoArray` | Sim | Matriz de informações de geração. |

## Exemplos {#section-fdffe6ed82d94c7aa90e47f7ce889403}

Esta amostra de código retorna informações sobre ativos gerados de um ativo específico. Ele não recupera informações sobre as etapas usadas para gerar o ativo especificado. A resposta é truncada por brevidade.

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
