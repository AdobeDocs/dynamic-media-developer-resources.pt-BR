---
description: Define o mapa de imagem de um ativo.
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# setImageMaps{#setimagemaps}

Define o mapa de imagem de um ativo.

Você já deve ter criado os mapas de imagem. Os mapas de imagem são aplicados na ordem de recuperação da matriz. Isso significa que o segundo mapa de imagem se sobrepõe ao primeiro, o terceiro se sobrepõe ao segundo e assim por diante.

## Tipos de usuário autorizados {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-2292ec1aead947ef8741dd0653a41f42}

**Entrada (setImageMapsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | Identificador da empresa. |
| assetHandle | `xsd:string` | Sim | Identificador de ativo. |
| imageMapArray | `types:ImageMapDefinitionArray` | Sim | Matriz de mapas de imagem predefinidos. |

**Saída (setImageMapsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| imageMapHandleArray | `types:HandleArray` | Sim | Uma matriz com alças de mapa de imagem aplicadas ao ativo. |

## Exemplos {#section-fe2e35662a6a4ee29cf250c9fd180371}

Essa amostra de código define dois mapas de imagem para um ativo de imagem. O código especifica o tipo de forma, a região e a ação executada quando os mapas de imagem são invocados. A resposta contém uma matriz com identificadores para os mapas de imagem.

**Solicitação**

```java
<setImageMapsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <imageMapArray>
      <items>
         <name>ImageMap2</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>true</enabled>
      </items>
      <items>
         <name>ImageMap3</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>false</enabled>
      </items>
   </imageMapArray>
</setImageMapsParam>
```
