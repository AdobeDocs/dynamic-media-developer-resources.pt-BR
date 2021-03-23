---
description: Define o mapa de imagem de um ativo.
seo-description: Define o mapa de imagem de um ativo.
seo-title: setImageMaps
solution: Experience Manager
title: setImageMaps
uuid: 1dd7e032-34b4-464d-8ec6-7ad282d12891
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# setImageMaps{#setimagemaps}

Define o mapa de imagem de um ativo.

Você já deve ter criado os mapas de imagem. Mapas de imagem são aplicados na ordem de recuperação da matriz. Isso significa que o segundo mapa de imagem se sobrepõe ao primeiro, o terceiro se sobrepõe ao segundo e assim por diante.

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
| `*`companyHandle`*` | `xsd:string` | Sim | Manuseio da empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | Identificador de ativo. |
| `*`imageMapArray`*` | `types:ImageMapDefinitionArray` | Sim | Matriz de mapas de imagem predefinidos. |

**Saída (setImageMapsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`imageMapHandleArray`*` | `types:HandleArray` | Sim | Uma matriz com identificadores de mapa de imagem aplicados ao ativo. |

## Exemplos {#section-fe2e35662a6a4ee29cf250c9fd180371}

Essa amostra de código define 2 mapas de imagem para um ativo de imagem. O código especifica o tipo de forma, a região e a ação executada quando os mapas de imagem são chamados. A resposta contém uma matriz com identificadores para os mapas de imagem.

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

