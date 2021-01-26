---
description: Define o mapa de imagem para um ativo.
seo-description: Define o mapa de imagem para um ativo.
seo-title: setImageMaps
solution: Experience Manager
title: setImageMaps
topic: Dynamic Media Image Production System API
uuid: 1dd7e032-34b4-464d-8ec6-7ad282d12891
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---


# setImageMaps{#setimagemaps}

Define o mapa de imagem para um ativo.

Você já deve ter criado os mapas de imagem. Os mapas de imagem são aplicados na ordem de recuperação da matriz. Isso significa que o segundo mapa de imagem sobrepõe o primeiro, o terceiro sobrepõe o segundo e assim por diante.

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
| `*`companyHandle`*` | `xsd:string` | Sim | Alça da empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | Identificador de ativos. |
| `*`imageMapArray`*` | `types:ImageMapDefinitionArray` | Sim | Matriz de mapas de imagem predefinidos. |

**Saída (setImageMapsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`imageMapHandleArray`*` | `types:HandleArray` | Sim | Uma matriz com alças de mapa de imagem aplicadas ao ativo. |

## Exemplos {#section-fe2e35662a6a4ee29cf250c9fd180371}

Esta amostra de código define 2 mapas de imagem para um ativo de imagem. O código especifica o tipo de forma, a região e a ação executada quando os mapas de imagem são chamados. A resposta contém uma matriz com alças para os mapas de imagem.

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

