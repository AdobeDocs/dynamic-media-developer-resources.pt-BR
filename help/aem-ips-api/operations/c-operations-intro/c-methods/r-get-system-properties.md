---
description: Recupera todas as propriedades do sistema em uma única solicitação.
seo-description: Recupera todas as propriedades do sistema em uma única solicitação.
seo-title: getSystemProperties
solution: Experience Manager
title: getSystemProperties
topic: Dynamic Media Image Production System API
uuid: 08ea86ba-bde5-45a1-920a-04f784395e6a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---


# getSystemProperties{#getsystemproperties}

Recupera todas as propriedades do sistema em uma única solicitação.

Sintaxe

## Tipos de usuário autorizados {#section-fc311ce90a54400fa95b9dd36b756e23}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Parâmetros {#section-b2a4fb7068424223aec87c50f0586d73}

**Entrada (getSystemPropertiesParam)**

Nenhum.

**Saída (getSystemPropertiesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`propertyArray`*` | `types:PropertyArray` | Sim | Uma matriz de propriedades do sistema. |

## Exemplos {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

Essa amostra de código retorna uma matriz de propriedades do sistema. Resposta truncada para brevidade.

**Solicitação**

```java
<getSystemPropertiesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"/>
```

**Resposta**

```java
<getSystemPropertiesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"> 
   <propertyArray> 
      <items> 
         <name>SvgRenderEnabled</name> 
         <value>true</value> 
      </items> 
      <items> 
         <name>SwfRootUrl</name> 
         <value>/SWFs/</value> 
      </items> 
      ... 
   </propertyArray> 
</getSystemPropertiesReturn>
```

