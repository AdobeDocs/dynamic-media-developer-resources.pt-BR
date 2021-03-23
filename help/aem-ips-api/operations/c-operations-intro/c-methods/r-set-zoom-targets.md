---
description: Define o direcionamento de zoom associado a uma imagem de ativo. Substitui os destinos de zoom existentes.
seo-description: Define o direcionamento de zoom associado a uma imagem de ativo. Substitui os destinos de zoom existentes.
seo-title: setZoomTargets
solution: Experience Manager
title: setZoomTargets
uuid: 5d0aecec-ebd8-4c69-9514-c29fae347ee6
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# setZoomTargets{#setzoomtargets}

Define o direcionamento de zoom associado a uma imagem de ativo. Substitui os destinos de zoom existentes.

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
| `*`companyHandle`*` | `xsd:string` | Sim | Manuseio da empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | Ativo com o direcionamento de zoom que você deseja definir. |
| `*`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | Sim | Matriz de definições de direcionamento de zoom. |

**Saída (setZoomTargetsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`zoomTargetHandleArray`*` | `types:HandleArray` | Sim | O conjunto de identificadores para os destinos de zoom criados por esta operação. |

## Exemplos {#section-a2f14c7a1499443e96d099ea8a76c182}

Essa amostra de código define uma matriz de destinos de zoom por nome, posição (eixo x e y), largura, altura e atribui a matriz a um ativo. A resposta contém identificadores para os destinos de zoom recém-criados.

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

