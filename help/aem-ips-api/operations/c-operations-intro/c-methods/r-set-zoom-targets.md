---
description: Define o público alvo de zoom associado a uma imagem de ativo. Substitui os públicos alvos de zoom existentes.
seo-description: Define o público alvo de zoom associado a uma imagem de ativo. Substitui os públicos alvos de zoom existentes.
seo-title: setZoomTargets
solution: Experience Manager
title: setZoomTargets
topic: Scene7 Image Production System API
uuid: 5d0aecec-ebd8-4c69-9514-c29fae347ee6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# setZoomTargets{#setzoomtargets}

Define o público alvo de zoom associado a uma imagem de ativo. Substitui os públicos alvos de zoom existentes.

Sintaxe

## Tipos de usuário autorizados {#section-c5e1863e9cb1426591bfea513620b6ab}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-161f8c733cc4439f94a06e12119d4226}

**Entrada (setZoomTargetsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sim | Alça da empresa. |
| ` *`assetHandle`*` | `xsd:string` | Sim | Ativo com o público alvo de zoom que você deseja definir. |
| ` *`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | Sim | Matriz de definições de públicos alvos de zoom. |

**Saída (setZoomTargetsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`zoomTargetHandleArray`*` | `types:HandleArray` | Sim | O conjunto de identificadores para os públicos alvos de zoom criados por esta operação. |

## Exemplos {#section-a2f14c7a1499443e96d099ea8a76c182}

Essa amostra de código define uma matriz de públicos alvos de zoom por nome, posição (eixo x e y), largura, altura e atribui a matriz a um ativo. A resposta contém identificadores para os públicos alvos de zoom recém-criados.

**Solicitação**

```java
<setZoomTargetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <zoomTargetArray>
      <items>
         <name>zoomTarget2</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
      <items>
         <name>zoomTarget3</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
   </zoomTargetArray>
</setZoomTargetsParam>
```

**Resposta**

```java
<setZoomTargetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zoomTargetHandleArray>
      <items>a|947|9|41</items>
      <items>a|948|9|42</items>
   </zoomTargetHandleArray>
</setZoomTargetsReturn>
```

