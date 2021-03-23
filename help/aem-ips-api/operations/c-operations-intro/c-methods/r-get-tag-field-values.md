---
description: Obtém todos os valores de dicionário de tags definidos para um ou mais campos de tag.
seo-description: Obtém todos os valores de dicionário de tags definidos para um ou mais campos de tag.
seo-title: getTagFieldValues
solution: Experience Manager
title: getTagFieldValues
uuid: 92d84dfc-6a6c-4876-9670-1152adb6317c
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# getTagFieldValues{#gettagfieldvalues}

Obtém todos os valores de dicionário de tags definidos para um ou mais campos de tag.

Sintaxe

## Tipos de usuário autorizados {#section-cc36a437394c491594e704a08a161c87}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-9ad806e7736e4d51ae42cad185050cf9}

**Entrada (getTagFieldValuesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que contém o campo de tag. |
| `*`fieldHandleArray`*` | `types:HandleArray` | Sim | Uma matriz de campo trata os valores de tag que você deseja retornar. |

**Saída (getTagFieldValuesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`fieldArray`*` | `types:TagFieldValuesArray` | Sim | Uma matriz dos valores da tag no dicionário para cada campo solicitado. |

## Exemplos {#section-4492742614e44bb191a7d397dc1a1407}

**Solicitação**

```java
<getTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandleArray>
      <items>m|3|ASSET|SingleOpenTag</items>
      <items>m|3|ASSET|SingleFixedTag</items>
   </fieldHandleArray>
</getTagFieldValuesParam>
```

**Resposta**

```java
<getTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <fieldArray>
      <items>
         <fieldHandle>m|3|ASSET|SingleOpenTag</fieldHandle>
         <valueArray>
            <items>GroupB</items>
            <items>GroupA</items>
         </valueArray>
      </items>
      <items>
         <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
         <valueArray>
            <items>North</items>
            <items>South</items>
            <items>East</items><items>West</items>
         </valueArray>
      </items>
   </fieldArray>
</getTagFieldValuesReturn>
```

